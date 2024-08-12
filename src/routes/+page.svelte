
<section>

    <h1>Personal info</h1>
    <h3>Please provide your name, email address and phone number.</h3>

    <form action="">
        <div>
            <label for="name">Name</label>
            <input type="text" name="name" placeholder="e.g. Stephen King">
        </div>
        <div>
            <label for="name">Email</label>
            <input type="email" name="email" id="" placeholder="e.g. stephenking@lorem.com">
        </div>
        <div>
            <label for="name">Phone Number</label>
            <input type="tel" name="phoneNumber" id="" placeholder="e.g. +1 234 567 890">
        </div>
    </form>
</section>

<style>
    section {
        background-color: var(--white);
        padding: 30px;
        border-radius: 10px;
        z-index: 100;
        margin: 15px;
        position: relative;
        margin-top: 25px;
        display: flex;
        flex-direction: column;
        gap: 15px;
    }

    section h1 {
        font-family: "Ubuntu", sans-serif;
        color: var(--marine-blue);
        font-weight: 900;
    }

    section h3 {
        font-weight: 500;
        color: var(--cool-gray);
        font-family: 'Ubuntu', sans-serif;
        font-size: 1.1rem;
    }

    form {
        display: flex;
        flex-direction: column;
        gap: 20px;
    }

    form div {
        display: flex;
        flex-direction: column;
        gap: 5px;
    }

    form div label {
        color: var(--marine-blue);
        font-weight: 600;
    }

    form div input {
        padding: 15px 20px;
        font-size: 1em;
        border: 1px solid var(--light-gray);
        border-radius: 7px;
        font-family: 'Ubuntu', sans-serif;
    }

    form div input:focus {
        outline: 1px solid var(--purplish-blue);
    }

    form div input::placeholder {
        font-weight: 600;
        color: var(--cool-gray);
    }

    @media screen and (width > 600px) {
        section {
            width: 80%;
            margin-left: auto;
            margin-right: auto;
        }
    }
</style>