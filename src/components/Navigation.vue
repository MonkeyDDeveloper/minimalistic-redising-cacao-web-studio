<template>
    <div>
        <nav class="navbar navbar-expand-lg bg-body-tertiary my-4">
            <div class="container-fluid">
                <router-link to="/" class="navbar-brand">
                    <img src="/CacaoLogoYellow.887ceb5.svg" width="130" alt="CocoWebStudio" class="d-inline align-text-top h-auto">
                </router-link>
                <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav"
                    aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
                    <span class="navbar-toggler-icon"></span>
                </button>
                <div class="collapse navbar-collapse" id="navbarNav">
                    <ul class="navbar-nav">
                        <li class="nav-item">
                            <router-link to="/projects" class="nav-link active" aria-current="page">Projects</router-link>
                        </li>
                        <li class="nav-item">
                            <router-link to="/services" class="nav-link">Services</router-link>
                        </li>
                        <li class="nav-item">
                            <router-link to="/contact-us" class="nav-link">Contact us</router-link>
                        </li>
                    </ul>
                </div>
            </div>
        </nav>
    </div>
</template>