<svelte:head>
	<title>Admin Login</title>
	<meta name="Login" content="Admin Login Page" />
</svelte:head>


<header class="top">
    <h1>One of us?</h1>
    <h3>Prove It!</h3>
</header>

<div class="container">
    <div class="loading">
        <div class="bar"></div>
        <div class="bar"></div>
        <div class="bar"></div>
        <div class="bar"></div>
        <div class="bar"></div>
        <div class="bar"></div>
        <div class="bar"></div>
        <div class="bar"></div>
    </div>
</div>

<div class="box">
    <form method="post">
        <h2>Email</h2>
        <input type="text" placeholder="Enter Email" name="uname" required>
        <h2>Password</h2>
        <input type="password" placeholder="Enter Password" name="psw" required>
        <br>
        <button type="submit">Login</button>
    </form>
</div>

<style>

    .top h1{
        text-align: center;
        padding-top: 1rem;
        margin: 0;
        font-size: 64px;
        background: linear-gradient(grey, red, orange);
        -webkit-background-clip: text;
        -webkit-text-fill-color: transparent;
    }

    .top h3{
        text-align: center;
        padding-top: 0.2rem;
        margin: 0;
        font-size: 35px;
        background: linear-gradient(grey, red, orange);
        -webkit-background-clip: text;
        -webkit-text-fill-color: transparent;
    }

    .container{
        display: flex;
        align-items: center;
        justify-content: center;
        height: 20vh;
    }

    .loading{
        width: 300px;
        height: 150px;
        position: relative;
        display: inline-flex;
        align-items: center;
        justify-content: space-between;
    }

    .loading .bar{
        width: 30px;
        border-radius: 20px;
        background: rgba(255, 255, 255, 0.736);
        animation: movement 1.5s ease-in-out infinite;
    }

    @keyframes movement{
        0%, 100%{
            height: 4px;
        }
        50%{
            height: 70px;
        }
    }

    .loading .bar:nth-child(1){
        background: red;
        animation-delay: .2s;
    }
    .loading .bar:nth-child(2){
        background: orange;
        animation-delay: .4s;
    }
    .loading .bar:nth-child(3){
        background: yellow;
        animation-delay: .5s;
    }
    .loading .bar:nth-child(4){
        background: lime;
        animation-delay: .6s;
    }
    .loading .bar:nth-child(5){
        background: lime;
        animation-delay: .6s;
    }
    .loading .bar:nth-child(6){
        background: yellow;
        animation-delay: .5s;
    }
    .loading .bar:nth-child(7){
        background: orange;
        animation-delay: .4s;
    }
    .loading .bar:nth-child(8){
        background: red;
        animation-delay: .2s;
    }

    .box{
        margin: 0 auto;
        width: 90%;
        max-width: 300px;
        background: rgba(255, 255, 255, 0.79);
        padding-top: 1.5rem;
        padding-bottom: 2.7rem;
        border-radius: 25%;
        text-align: center;
        border: groove rgb(223, 130, 17) 10px;
    }

    .box h2{
        text-align: center;
        margin: 0;
        font-size: 30px;
        background: linear-gradient(rgb(220, 156, 27), red, rgb(90, 88, 88));
        -webkit-background-clip: text;
        -webkit-text-fill-color: transparent;
        padding: 10px 0;
    }

    .box input{
        text-align: center;
        height: 30px;
        padding: 5px;
        border-radius: 25%;
    }

    .box button{
        margin-top: 25px;
        width: 100px;
        height: 30px;
        border: double rgb(54, 54, 54);
        border-radius: 20%;
    }

    .box button:hover, input:hover{
        color: red;
        background: black;
    }

</style>
