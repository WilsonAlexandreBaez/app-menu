<template>
  <div class="slider">
    <h1>{{ msg }}</h1>
    <div class="carousel-wrapper">
  <span id="item-1"></span>
  <span id="item-2"></span>
  <span id="item-3"></span>
  <div class="carousel-item item-1">
    <h2>Item 1</h2>
    <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vivamus   accumsan pretium dolor vel convallis. Aliquam erat volutpat. Maecenas lacus nunc, imperdiet sed mi et, finibus suscipit mi.</p>
    <a class="arrow arrow-prev" href="#item-3"></a>
    <a class="arrow arrow-next" href="#item-2"></a>
  </div>
  
  <div class="carousel-item item-2">
    <h2>Item 2</h2>
    <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vivamus accumsan pretium dolor vel convallis. Aliquam erat volutpat.</p>
    <a class="arrow arrow-prev" href="#item-1"></a>
    <a class="arrow arrow-next" href="#item-3"></a>
  </div>
  
  <div class="carousel-item item-3">
    <h2>Item 3</h2>
    <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vivamus accumsan pretium dolor vel convallis. Aliquam erat volutpat.</p>
    <a class="arrow arrow-prev" href="#item-2"></a>
    <a class="arrow arrow-next" href="#item-1"></a>
  </div>
</div>
  </div>
</template>

<script>
export default {
  name: 'JardimSlider',
  props: {
    msg: String
  }
}
</script>
<style scoped>
.carousel-wrapper{
  height:400px;
  position:relative;
  width:800px;
  margin:0 auto;
}
.carousel-item{
  position:absolute;
  top:0;
  bottom:0;
  left:0;
  right:0;
  padding:25px 50px;
  opacity:0;
  transition: all 0.5s ease-in-out;
}
.arrow{
  border: solid black;
    border-width: 0 3px 3px 0;
    display: inline-block;
    padding: 12px;
}

.arrow-prev{
  left:-30px;
  position:absolute;
  top:50%;
  transform:translateY(-50%) rotate(135deg);
}
 
.arrow-next{
    right:-30px;
  position:absolute;
  top:50%;
  transform:translateY(-50%) rotate(-45deg);
  }

.light{
  color:white;
}

@media (max-width: 480px) {
      .arrow, .light .arrow {
        background-size: 10px;
        background-position: 10px 50%;
      }
    }

/*Select every element*/
[id^="item"] {
    display: none;
  }

.item-1 {
    z-index: 2;
    opacity: 1;
  background:url('https://static.pexels.com/photos/6526/sea-beach-holiday-vacation-large.jpg');
  background-size:cover;
  }
.item-2{
  background:url('https://static.pexels.com/photos/6506/alcohol-bar-drinks-party-large.jpg');
   background-size:cover;
}
.item-3{
  background:url('https://static.pexels.com/photos/6529/lake-kajak-kayak-large.jpg');
   background-size:cover;
}

*:target ~ .item-1 {
    opacity: 0;
  }

#item-1:target ~ .item-1 {
    opacity: 1;
  }

#item-2:target ~ .item-2, #item-3:target ~ .item-3 {
    z-index: 3;
    opacity: 1;
  }



</style>