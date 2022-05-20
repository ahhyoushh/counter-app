<script>
    import Typewriter from 'svelte-typewriter'
    let count = 0;
    function add() {
        count += 1
    }
    function substract() {
        count -= 1
    }
</script>
<div class="container">
    <h1>Simple Counter app</h1>
    <div class="count">
        <h1>{count}</h1>
    </div>
    <Typewriter delay={1000}>
    <div class="github">
            <a href="https://github.com/Ayush32173">More Like This -></a>
    </div>
    </Typewriter>
    <div class="count-button">
        <button class="add" on:click={add}>Add</button>
        <button class="substract" on:click={substract}>substract</button>

    </div>

</div>

<style>
    @media only screen and (max-width: 480px) ,only screen and (max-device-width: 480px) {
        .count {
            font-size: 12px;
            display: flex;
            justify-content: center;
        }
    }
    .container .github > a {
        position: relative;
        color: #0059ff;
        top: 500px;
        display: flex;
        justify-content: center;
        transition: 300ms;
    }
    .container .github > a:hover {
        color: blue;
    }
    .container > h1 {
        color: white;
        position: fixed;
        top: 10px;
    }
    .count {
        position: absolute;
        font-size: 24px;
        top: 200px;
        justify-content: center;
        text-align: center;
        color: white;
    }
    .container .count-button .substract{
        font-size: 16px;
        padding: 16px 25px;
        border-radius: 15px;
    }
    .container .count-button .add{
        font-size: 16px;
        padding: 16px 38px;
        border-radius: 15px;

    }
    .container .count-button > button {
        background: none;
        outline: none;
        border: none;
        margin: 10px;
        color: white;
        background-color: #0059ff;
        transition: 300ms;
    }
    .container .count-button > button:hover {
        background-color: #0059ff44;
    }

    .container .count-button {

        position: fixed;
        top: 350px;
    }
    .container {
        font-family: 'Poppins', sans-serif;
        margin: none;
        display: flex;
        align-items: center;
        justify-content: center;
    }
</style>
