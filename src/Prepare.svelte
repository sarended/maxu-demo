<script>
    import Select from 'svelte-select';
    let showmain = true;
    const chandler = () => {
        showmain=false
    }
</script>

<style>
    main {
        width: 100vw;
        height: 100vh;
        overflow: hidden;
        font-family: 'Yekan',sans-serif;
        direction: rtl;
        display: flex;
        align-items: center;
        justify-content: center;
        background-color: #125488;
        background-image: url('/bg.png');
        background-size: cover;
        color: #505050;
    }
    .logo {
        position: absolute;
        top: 0px;
        right: 0px;
        width: 170px;
    }
    .container{
        /* border: 1px #ccc solid; */
        width: 500px;
        height: 500px;
        border-radius: 50px 0 0 50px;
        box-sizing: border-box;
        padding: 38px 150px 38px 50px;
        /* background-color: #2a93d5; */
        background-color: #fefefe;
        box-shadow: 0px 0px 50px silver;
        position: relative;
        right: -100px;
    }
    .items {
        display: flex;
        align-items: center;
        justify-content: space-between;
        margin-bottom: 5px;
    }
    .itemend {
        display: flex;
        justify-content: flex-end;
    }
    .yekan {
        font-family: 'Yekan', sans-serif;
        /* width: 60px; */
        text-align: center;
        color: #505050;
    }
    .btnc {
        display: flex;
        justify-content: center;
        align-items: center;
        padding: 20px;
    }
    .btn {
        font-family: 'Yekan', sans-serif;
        width: 85%;
        padding: 10px 5px;
        border: 0;
        border-radius: 5px;
        background-color: #2a93d5;
        color: white;
    }
    .imgp {
        width: 500px;
        height: 500px;
        object-fit: cover;
        border-radius: 50%;
        border: 10px solid #2a93d5;
        z-index: 100;
        position: relative;
        left: -30px;
    }
    .cpr {
        position: absolute;
        bottom: 0;
        display: flex;
        text-align: center;
        justify-content: center;
        align-items: center;
        padding-bottom: 2px;
        color: #505050;
    }
</style>

{#if showmain}
<main>
    <img class="logo" src="./cover2.png" alt="katoolaPAY">
    <img class="imgp" src="./item/papp.jpg" alt="عکس محصول">
    <div class="container">
        <div>
            <div class="items">
                <span> تعداد </span>
                <Select placeholder="انتخاب" items={['۱','۲']} class="yekan"></Select>
            </div>
            <div class="items">
                <span> انتخاب رنگ </span>
                <Select placeholder="انتخاب" items={['صورتی','قرمز']} class="yekan"></Select>
            </div>
            <div class="items">
                <span> انتخاب سایز </span>
                <Select placeholder="انتخاب" items={['۱','۲']} class="yekan"></Select>
            </div>
            <div class="items">
                <span> قیمت </span>
                <span>
                    <span> ۱۲۰,۰۰۰ </span>
                    <span> تومان </span>
                </span>
            </div>
            <div class="itemend">
                <span> ۱۱۰,۰۰۰ </span>
                <span> تومان </span>
            </div>
        </div>
        <div class="btnc">
            <button class="btn" on:click="{chandler}">خرید</button>
        </div>
    </div>
    <p class="cpr"> ۲۰۲۰ © کلیه حقوق این سایت برای کتولاپی محفوظ است. </p>
</main>
{/if}