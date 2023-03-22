<script lang="ts">
    import {base} from '$app/paths'
</script>

<div class="p-3 text-bg-dark">
    <nav class="container navbar navbar-expand-lg bg-dark">
        <div class="container-fluid">
            <a class="navbar-brand text-white" href="{base}/">Home</a>
            <div class="collapse navbar-collapse" id="navbarNav">
                <ul class="navbar-nav">
                    <li class="nav-item">
                        <a class="nav-link text-white" href="{base}/comic">Random Comic</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link text-white" href="{base}/about">About Project</a>
                    </li>
                </ul>
            </div>
        </div>
    </nav>
</div>
<div id="liveAlertPlaceholder"></div>