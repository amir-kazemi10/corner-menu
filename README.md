<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Document</title>
    <link rel="stylesheet" href="../assets/css/style-grid.css" />
    <script
      src="https://kit.fontawesome.com/0b315f45c8.js"
      crossorigin="anonymous"
    ></script>
    <style>
      p.title {
        display: flex;
        justify-content: center;
        align-items: center;
        padding: 100px;
        font-size: 34px;
      }
      body {
        background-color: rgb(240, 240, 240);
      }
      .circle-menu {
        position: fixed;
        bottom: 1em;
        right: 1em;
      }
      .menu-btn {
        display: block;
        width: 3.5em;
        height: 3.5em;
        border-radius: 50%;
        background-color: red;
        background-image: linear-gradient(-45deg, #A49DEF,#FBCCEC);
        color: #fff;
        cursor: pointer;
        text-align: center;
        line-height: 3.9em;
      }
      .active .menu-btn {
        box-shadow: 0 0 3px rgba(0, 0, 0, 0.3);
      }
      .active .menu-btn:active {
        box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.4);
      }
      .menu-btn i {
        font-size: 1.2em;
        transition: transform 0.2s ease;
      }
      .active .menu-btn i {
        transform: rotate(-45deg);
      }
      .circle-menu::after {
        content: "";
        display: block;
        width: 3.5em;
        height: 3.5em;
        border-radius: 50%;
        background-image: linear-gradient(145deg, #A49DEF,#FBCCEC);
        position: absolute;
        top: 0;
        right: 0;
        transition: all 0.3 ease;
        z-index: -2;
      }
      .active::after{
        transform: scale3d(5.5,5.5,1);
        transition:  0.3s ease ;
      }
      .menu-item{
        position: absolute;
        top: 0.2em;
        right: 0.2em;
        display: block;
        width: 3em;
        height: 3em;
        color: #fff;
        border-radius: 50%;
        text-align: center;
        line-height: 3;
        background-color: rgba(0, 0, 0, 0.1);
        transition: transform 0.3s ease,background-color 0.2s ease;
        z-index: -1;
      }
      .menu-item:hover{
        background-color:rgba(0, 0, 0, 0.3) ;
      }
      .active .item-wrapper .menu-item:nth-child(1){
transform: translate3d(1em,-7.2em,0);
      }
      .active .item-wrapper .menu-item:nth-child(2){
transform: translate3d(-3.5em,-6.3em,0);
      }
      .active .item-wrapper .menu-item:nth-child(3){
transform: translate3d(-6em,-3em,0);
      }
      .active .item-wrapper .menu-item:nth-child(4){
transform: translate3d(-7em,1em,0);
      }
      
    </style>
  </head>
  <body>
    <p class="title">پروژه شماره 7</p>
    <div class="circle-menu" id="circle-menu">
      <a class="menu-btn">
        <i class="fas fa-plus"></i>
      </a>
      <nav class="item-wrapper">
        <a href="" class="menu-item fas fa-home"></a>
        <a href="" class="menu-item fas fa-user"></a
        ><a href="" class="menu-item fas fa-chart-pie"></a>
        <a href="" class="menu-item fas fa-cog"></a>
      </nav>
    </div>

    <script
      src="https://code.jquery.com/jquery-3.7.1.min.js"
      integrity="sha256-/JqT3SQfawRcv/BIHPThkBvs0OEvtFFmqPF/lYI/Cxo="
      crossorigin="anonymous"
    ></script>
    <script>
        $(document).ready(function(){
    $(".menu-btn").click(function(){
        $("#circle-menu").toggleClass("active")
    })
})
    </script>
  </body>
</html>
