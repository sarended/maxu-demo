<script>
    let showmain = true;
    const chandler = () => {
        showmain=false
    }
</script>

<style>
    main {
        width: 100%;
        height: 100vh;
        overflow: hidden;
    }
    .ig {
        background-color: #f5f5f5;
        height: 50px;
        font-size: 1.5rem;
        font-family: cursive;
        text-align: center;
        border-bottom: 1px solid #ccc;
        display: flex;
        align-items: center;
        justify-content: center;
    }
    div {
        width: 100%;
    }
    img {
        max-height: 550px;
    }
    .imgholder {
        background-color: black;
        display: flex;
        align-items: center;
        justify-content: center;
    }
    .nav {
        position: absolute;
        bottom: 0;
        height: 50px;
        font-size: 1.7rem;
        display: flex;
        justify-content: space-evenly;
        width: 100%;
        align-items: center;
        border-top: #ccc 1px solid;
        background-color: white;
    }
    .deactive{
        color: silver;
    }
    .tools {
        font-size: 1.5rem;
        padding-left: 10px;
        padding-top: 5px;
    }
    .fared {
        color: red;
    }
    .buy {
        color: blue;
        font-weight: bold;
        cursor: pointer;
    }
    .user {
        /* margin-left: 20px; */
        display: flex;
        justify-content: space-between;
        align-items: center;
        padding: 5px 10px;
        width: calc(100% - 20px);
    }
</style>

{#if showmain}
<main>
    <div class="ig">
        <p>instagram</p>
    </div>
    <div>
        <div class="user">
            <div>
                <i class="fas fa-user deactive"/>
                <span> khalili</span>
            </div>
            <i class="fas fa-ellipsis-h"></i>
        </div>
        <div class="imgholder">
            <img src="./item/p1.webp" alt="pink short">
        </div>
        <div class="tools">
            <i class="fas fa-heart fared"/>
            <i class="far fa-comment"/>
            <i class="fas fa-share"/>
        </div>
        <div>
            <span>description description description description description
               description description description description description
               description description description description description
               description description description description description
               description description description
            </span>
            <span class="buy" on:click="{chandler}">bekharid</span>
        </div>
    </div>
    <div class="nav">
        <i class="fas fa-home"/>
        <i class="fas fa-search deactive"/>
        <i class="fas fa-camera deactive"/>
        <i class="far fa-heart deactive"/>
        <i class="fas fa-user deactive"/>
    </div>
</main>
{/if}