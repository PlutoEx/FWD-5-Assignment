<script>
	// import RandomJoke from "./+page.svelte";
</script>

<svelte:head>
	<title>5 Assignment</title>
	<meta name="description" content="Portfolio" />

</svelte:head>

<div class="container">
	<div class="row">
		<div class="col-3"></div>
		<div class="col-7">
			<ul class="nav nav-tabs" id="myTab">
				<li class="nav-item" role="presentation">
					<button class="nav-link active" id="profile-tab" data-bs-toggle="tab" data-bs-target="#profile-tab-pane" type="button" role="tab" aria-controls="profile-tab-pane" aria-selected="false">Profile</button>
				</li>
				<li class="nav-item" role="presentation">
					<button class="nav-link" id="projects-tab" data-bs-toggle="tab" data-bs-target="#projects-tab-pane" type="button" role="tab" aria-controls="projects-tab-pane" aria-selected="false">Projects</button>
				</li>
			</ul>
		</div>
	</div>
	<div class="row">
		<div class="col-3 justify-content-center">
			<div class="my-avatar">
				<i class="bi bi-person-circle"></i>
			</div>
			<div>
				<strong class="d-block">Arlan Kuralbayev</strong>
				<a href="mailto:name.surname.best.07@gmail.com">My email</a>
			</div>
		</div>
		<div class="col-7">
			<div class="tab-content" id="myTabContent">
				<div class="tab-pane fade show active" id="profile-tab-pane" role="tabpanel" aria-labelledby="profile-tab" tabindex="0">
					<div>
						<h1>Profile</h1>
						<p>My name is Arlan Kuralbayev</p>
						<!-- TODO auto update age -->
						<span id="my-age">20</span> y.o. Software Developer from somecity, KZ
						<div>
							My languages:
							<ul>
								<!-- TODO make ratio -->
								<li>C, C++</li>
								<li>Java</li>
								<li>JavaScript</li>
								<li>SomeScript</li>
								<li>SomeLang#</li>
								<li>Eng, Rus, Kz</li>
							</ul>
						</div>
						<div>
							My achievements:
							<ul>
								<li>:( No Achievements</li>
							</ul>
						</div>
					</div>
				</div>
				<div class="tab-pane fade" id="projects-tab-pane" role="tabpanel" aria-labelledby="projects-tab" tabindex="0">
					<div>
						<h1>Projects</h1>
						later, hope this is enough
					</div>
				</div>
			</div>
		</div>
	</div>
</div>

<style>
	.bi-person-circle {
		font-size: 140px;
		color: black;
	}
</style>
