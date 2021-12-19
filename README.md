# Selektory

<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>11-урок</title>
</head>
<body>
    <div class="post-wrap">
        <div class="post-item">
        <div class="item-content">
        <div class="item-icon group"></div>
        <div class="item-body">
        <h3>Иш чара</h3>
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla feugiat a quam non blandit.</p>
        </div>
        <div class="item-footer">
        <a href="#" class="link"><span>Подробнее</span></a>
        </div>
        </div>
        </div>
        
        <div class="post-item">
        <div class="item-content">
        <div class="item-icon tree"></div>
        <div class="item-body">
        <h3>Эс алуу</h3>
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla feugiat a quam non blandit.</p>
        </div>
        <div class="item-footer">
        <a href="#" class="link"><span>Подробнее</span></a>
        </div>
        </div>
        </div>
        
        <div class="post-item">
        <div class="item-content">
        <div class="item-icon anchor"></div>
        <div class="item-body">
        <h3>Футбол</h3>
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla feugiat a quam non blandit.</p>
        </div>
        <div class="item-footer">
        <a href="#" class="link"><span>Подробнее</span></a>
        </div>
        </div>
        </div>
        
        <div class="post-item">
        <div class="item-content">
        <div class="item-icon video"></div>
        <div class="item-body">
        <h3>Видео</h3>
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla feugiat a quam non blandit.</p>
        </div>
        <div class="item-footer">
        <a href="#" class="link"><span>Подробнее</span></a>
        </div>
        </div>
        </div>
        
        <div class="post-item">
        <div class="item-content">
        <div class="item-icon photo"></div>
        <div class="item-body">
        <h3>Фото</h3>
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla feugiat a quam non blandit.</p>
        </div>
        <div class="item-footer">
        <a href="#" class="link"><span>Подробнее</span></a>
        </div>
        </div>
        </div>
        
        <div class="post-item">
        <div class="item-content">
        <div class="item-icon gift"></div>
        <div class="item-body">
        <h3>Белек</h3>
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla feugiat a quam non blandit.</p>
        </div>
        <div class="item-footer">
        <a href="#" class="link"><span>Подробнее</span></a>
        </div>
        </div>
        </div>
        </div>
</body>
</html>

CSS
* {
   margin: 0;
   box-sizing: border-box;
}
body {
   background: #39383F;
   font-family: 'Montserrat Alternates', sans-serif;
}
.post-wrap {
   max-width: 1120px;
   margin: 0 auto;
   display: flex;
   justify-content: center;
   flex-wrap: wrap;
}
.post-item {
   padding: 15px;
   cursor: pointer;
}
.post-item * {
   transition: .3s linear;
}
.item-content {
   background: #413D4C;
   padding: 40px;
}
.item-icon {
   margin-bottom: 20px;
}
.item-icon:before {
   content: "";
   font-family: FontAwesome;
   color: #F09EA3;
   font-size: 50px;
   line-height: 1;
}
.item-icon.photo:before {
   content: "\f030";
}
.item-icon.video:before {
   content: "\f03d";
}
.item-icon.gift:before {
   content: "\f06b";
}
.item-icon.group:before {
   content: "\f0c0";
}
.item-icon.tree:before {
   content: "\f1bb";
}
.item-icon.anchor:before {
   content: "\f13d";
}
.post-item:hover .item-icon, .post-item:hover .item-body h3, .post-item:hover .item-body p {
   transform: translateY(-8px);
}
.item-body {
   color: #F5E2CD;
   font-size: 14px;
}
.item-body h3 {
   font-weight: 500;
   margin-bottom: 15px;
   transition-delay: .05s;
}
.item-body p {
   transition-delay: .1s;
}
.item-footer {
   padding-top: 15px;
}
.link {
   text-decoration: none;
   display: inline-block;
   overflow: hidden;
   position: relative;
   padding-right: 30px;
   font-size: 12px;
   text-transform: uppercase;
   font-weight: 600;
   color: #F5E2CD;
}
.link:before {
   content: "";
   position: absolute;
   top: 0;
   left: 0;
   width: 100%;
   bottom: 0;
   height: .125rem;
   margin: auto;
   background: #F09EA3;
   transform: scaleX(.2);
   transform-origin: left center;
   z-index: 0;
   transition: .6s cubic-bezier(.6, .01, 0, 1);
}
.link span {
   display: inline-block;
   position: relative;
   transform: translateX(-200%);
   transition: .6s cubic-bezier(.6, .01, 0, 1);
}
.post-item:hover .link span {
   transform: translateX(0%);
}
.post-item:hover .link:before {
   transform-origin: right center;
}
@media (min-width: 768px) {
   .post-item {
      flex-basis: 50%;
      flex-shrink: 0;
   }
}
@media (min-width: 960px) {
   .post-item {
      flex-basis: 33.333333333%;
   }
}
