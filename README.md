<h1>Hello! Welcome to my repository</h1>
-->
<h1 class="strip">
  Hello<br>
  Wellocome to my<br>
  repository
<h1>
 $bg-color: linear-gradient(15deg, #00a9f1, #cf00f1);
$text-color: #fff;

body {
  height: 100vh;
  background: $bg-color;
  color: $text-color;
  position: relative;
  
  &:before {
    content: 'CLICK';
    font-family: 'Roboto';
    font-size: 15px;
    color: rgba(255, 255, 255, 1);
    position: absolute;
    z-index: 10;
    right: 30px;
    top: 30px;
    
    @media (max-width: 480px) {
      top: auto;
      bottom: 20px;
      right: 20px;
    }
  }
}

h1 {
  font-family: Roboto, sans-serif;
  font-weight: 100;
  font-size: 100px;
  margin: 0;
  padding: 30px;
  text-transform: uppercase;
  
  @media (max-width: 700px) {
    padding: 20px;
    font-size: 40px;
  }

  span {
    display: inline-block;
    transition: transform .6s cubic-bezier(.65,.02,.23,1);
    transform: translate(20%, 100%);
    position: relative;
    z-index: 1;
    letter-spacing: -0.03em;
    text-shadow: 3px 4px 0 rgba(0, 0, 0, .1);
    
    &:before {
      content: '';
      position: absolute;
      z-index: 1;
      bottom: 0;
      left: 0;
      width: 100%;
      height: 100%;
      transform: translateY(-40%);
      transition: transform .6s cubic-bezier(.65,.02,.23,1);
    }
    
    &.row {
      overflow: hidden;
      line-height: 0.9;
      display: block;
      transform: none;
      
      &:before {
        display: none;
      }
    }
  }

  .animate {
    transform: translate(0, 0);
    
    &:before {
      transform: translateY(100%);
    }
  }
}
 $('.strip').each(function(){
  var $t = $(this),
      rows = $.trim($t.html()).split('<br>');

  $t.html('');

  $.each(rows, function(i, val){
    $('<span class="row"></span>').appendTo($t);

    var letters = $.trim(val).split('');

    $.each(letters, function(j, v){
      v = (v == ' ') ? '&nbsp;' : v;
      $('<span>' + $.trim(v) + '</span>').appendTo($('.row:last', $t));
    });

  });
});

$('body').click(function(){
  for (i = 0; i < $('.strip span').length; i++) {
    (function(ind) {
      setTimeout(function(){
          $('.strip span:not(".row")').eq(ind).toggleClass('animate');
      }, ind * 15);
    })(i);
  }
}).click();


<img  src="https://raw.githubusercontent.com/devicons/devicon/1119b9f84c0290e0f0b38982099a2bd027a48bf1/icons/javascript/javascript-original.svg" alt="JavaScript" width="50" height="50"/> &nbsp;<img  src="https://raw.githubusercontent.com/devicons/devicon/1119b9f84c0290e0f0b38982099a2bd027a48bf1/icons/nodejs/nodejs-plain.svg" alt="NodeJS" width="50" height="50"/> &nbsp;<img  src="https://github.com/CyrisXD/CyrisXD/raw/master/assets/ExpressJS.png" alt="ExpressJS"/> &nbsp; <img  src="https://raw.githubusercontent.com/devicons/devicon/1119b9f84c0290e0f0b38982099a2bd027a48bf1/icons/react/react-original.svg" alt="ReactJS" width="50" height="50" style="margin:0 auto; display:block;"/> &nbsp;<img  src="https://github.com/CyrisXD/CyrisXD/raw/master/assets/NextJS.png" alt="NextJS"/> &nbsp; <img  src="https://github.com/CyrisXD/CyrisXD/raw/master/assets/TailwindCSS.png" alt="TailwindCSS"/> &nbsp;<img src="https://raw.githubusercontent.com/devicons/devicon/1119b9f84c0290e0f0b38982099a2bd027a48bf1/icons/firebase/firebase-plain-wordmark.svg" alt="Firebase" width="50" height="50"/> &nbsp;<img  src="https://raw.githubusercontent.com/devicons/devicon/1119b9f84c0290e0f0b38982099a2bd027a48bf1/icons/vscode/vscode-original.svg" alt="VSCode" width="50" height="50"/> &nbsp;<img  src="https://github.com/CyrisXD/CyrisXD/raw/master/assets/Github.png" alt="Github"/> &nbsp;<img  src="https://raw.githubusercontent.com/devicons/devicon/1119b9f84c0290e0f0b38982099a2bd027a48bf1/icons/html5/html5-plain.svg" alt="HTML5" width="50" height="50"/> &nbsp;<img  src="https://raw.githubusercontent.com/devicons/devicon/1119b9f84c0290e0f0b38982099a2bd027a48bf1/icons/css3/css3-original.svg" alt="CSS3" width="50" height="50"/>

<!-- <p align="center">
 
</p> -->


<!--
**Aveek-Saha/aveek-saha** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->
