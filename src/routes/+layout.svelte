<script>
    import { page } from "$app/stores"
    import sidebarImg from '$lib/assets/bg-sidebar-mobile.svg'
    import Footer from '$lib/components/Footer.svelte'

</script>

<main>
    <img src={sidebarImg} alt="sidebar" class="sidebarImage">
    <nav>
        <div class={$page.url.pathname == "/" ? "currentPath" : ""}>
            <a href="/">
                <h2>
                    1
                </h2>
            </a>
        </div>
        <div class={$page.url.pathname == "/step/2" ? "currentPath" : ""}>
            <a href="/step/2">
                <h2>
                    2
                </h2>
            </a>
        </div>
        <div class={$page.url.pathname == "/step/3" ? "currentPath" : ""}>
            <a href="/step/3">
                <h2>
                    3
                </h2>
            </a>
        </div>
        <div class={$page.url.pathname == "/step/4" ? "currentPath" : ""}>
            <a href="/step/4">
                <h2>
                    4
                </h2>
            </a>
        </div>
    </nav>
    <slot></slot>

    <Footer />

    
</main>





<style>
    :global(*) {
        margin: 0px;
    }
    :global(:root) {
        --marine-blue: hsl(213, 96%, 18%);
        --purplish-blue: hsl(243, 100%, 62%);
        --pastel-blue: hsl(228, 100%, 84%);
        --light-blue: hsl(206, 94%, 87%);
        --strawberry-red: hsl(354, 84%, 57%);

        /* Neutral Colors */
        --cool-gray: hsl(231, 11%, 63%);
        --light-gray: hsl(229, 24%, 87%);
        --magnolia: hsl(217, 100%, 97%);
        --alabaster: hsl(231, 100%, 99%);
        --white: hsl(0, 0%, 100%);

        font-size: 16px;
        font-family: "Ubuntu", sans-serif;
    }

    :global(a) {
        text-decoration: none;
    }

    nav {
        display: flex;
        gap: 15px;
        justify-content: center;
        margin-top: -140px;
    }

    .currentPath {
        background-color: var(--light-blue);
        border-color: var(--light-blue);
        color: var(--marine-blue);
    }

    

    

    .sidebarImage {
        width: 100%;
    }

    main {
        background-color: var(--magnolia);
        min-height: 100vh;
    }

    

    nav div {
        color: var(--white);
        border: 2px solid var(--magnolia);
        width: 35px;
        height: 35px;
        border-radius: 50%;
        display: flex;
        justify-content: center;
        align-items: center;

        & h2 {
            font-size: 1em;
        }

        & a {
            text-decoration: none;
            color:inherit;
        }
    }

    main > img {
        z-index: -100;
    }





    @media screen and (width > 430px) {
        nav {
            margin-top: -170px;
        }
    }
    @media screen and (width > 550px) {
        nav {
            margin-top: -200px;
        }
    }
</style>