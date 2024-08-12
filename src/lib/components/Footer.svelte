<script>
    import { page } from '$app/stores'
</script>

{#snippet footerBtn(step)}
    <a href={step == 2 ? "/" : "/step/" + `${step - 1}`}><p class="backLink">Go Back</p></a>
    <a href={step == 4 ? "" : "/step/" + `${step + 1}`}><button class="nextStep">Next Step</button></a>
{/snippet}

<footer>
    {#if $page.url.pathname == "/"}
        <p></p>
        <a href="/step/2"><button class="nextStep">Next Step</button></a>
    {:else if $page.url.pathname == "/step/2"}
        {@render footerBtn(2)}
    {:else if $page.url.pathname == "/step/3"}
        {@render footerBtn(3)}
    {:else if $page.url.pathname == "/step/4"}
        {@render footerBtn(4)}
    {/if}
</footer>

<style>
    footer {
        background-color: var(--white);
        position: fixed;
        bottom: 0;
        padding: 20px;
        width: 90%;
        display: flex;
        justify-content: space-between;
        align-items: center;
    }

    .nextStep {
        color: var(--white);
        background-color: var(--marine-blue);
        padding: 15px 20px;
        font-family: "Ubuntu", sans-serif;
        font-size: 1.1em;
        border: none;
        border-radius: 8px;
        cursor: pointer;
        /* font-weight: 600; */

        &:hover {
            background-color: hsla(213, 96%, 18%, 0.91);
        }

        
    }

    .backLink {
        color: var(--cool-gray);
        font-family: "Ubuntu", sans-serif;
        font-weight: 600;
    }

    @media screen and (width > 430px) {
        footer {
            width: 93%;
        }
    }
    @media screen and (width > 550px) {
        footer {
            width: 95%;
        }
    }
</style>