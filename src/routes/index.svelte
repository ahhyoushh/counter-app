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
    <Typewriter delay={200}>
        <p style="color: #0059ff; position: fixed; top: 70px; left: 430px">I made this app to get the svelte basics done , dont judge me.</p>
    </Typewriter>
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
    .container .github > a {
        position: fixed;
        color: #0059ff;
        top: 600px;
        left: 620px;
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
        position: fixed;
        font-size: 24px;
        top: 200px;
        justify-content: center;
        text-align: center;
        left: 660px;
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