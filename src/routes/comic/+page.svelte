<script lang="ts">
    const email: string = 'a.kuralbayev@innopolis.university'
    let id: number = 0
    let myImg: string = ''
    let myImgAlt: string = ''
    let imgTitle: string = ''
    let imgAlt: string = ''
    let imgDate: string = ''

    async function fetchId(): Promise<number> {
        return await fetch('https://fwd.innopolis.app/api/hw2?email=' + email).then(r => r.json());
    }

    async function fetchImage(id: string): Promise<Comic> {
        return fetch('https://getxkcd.vercel.app/api/comic?num=' + id).then(r => r.json());
    }

    interface Comic {
        img: string
        alt: string
        day: string
        month: string
        year: string
        title: string
    }

    function handleComic(data: Comic) {
        myImg = data.img
        myImgAlt = data.alt
        imgTitle = 'Title: ' + data.title
        imgAlt = 'Alt: ' + data.alt
        const date = new Date(parseInt(data.year), parseInt(data.month) - 1, parseInt(data.day)).toLocaleDateString();
        imgDate = 'Date: ' + date
    }

    async function start () {
        id = await fetchId()
        const data: Comic = await fetchImage(id.toString())
        handleComic(data)
    }

    start()

    const randomIdBtn = async () => {
        id = Math.floor(Math.random() * 1000)
        const data: Comic = await fetchImage(id.toString())
        handleComic(data)
    }
</script>

<svelte:head>
    <title>Random Comic</title>
    <meta name="description" content="Random comic from API" />
</svelte:head>

<div class="container">
    <h1>Random Comic</h1>
    <div>
        <div id="myId"></div>
        <button type="button" class="btn btn-primary" id="getId" on:click={randomIdBtn}>Get Random ID</button>
        <div class="d-inline-block">{id}</div>
    </div>
    <div style="align-content: stretch; align-items: stretch;">
        <div>{imgTitle}</div>
        <div>{imgDate}</div>
        <div>{imgAlt}</div>
    </div>
    <img src="{myImg}" alt="{myImgAlt}">
</div>