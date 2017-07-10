# Homepage
<p>Copyright @2017, CC License</p>
<!-- To change theme, replace its name in following 4 lines  -->
<p>
<script type="text/javascript">// <![CDATA[
var mascotPath = "themes/ruri-dark/images/mascots/";
// ]]></script>
<script src="themes/ruri-dark/mascots.js" type="text/javascript"></script>
<script src="js/jquery-2.1.1.min.js" type="text/javascript"></script>
<script src="js/mascots-control.js" type="text/javascript"></script>
</p>
<header>
<h1>A Room with Views <span class="name-highlight">, Y</span></h1>
<p class="subtitle">Small Number, Big Ideas</p>
</header>
<section class="searchContainer"><form class="searchForm" action="https://google.com/search" method="get"><input class="searchBar search_google" name="q" type="text" autofocus="autofocus" placeholder="Google" /></form><form class="searchForm" action="https://youtube.com/results" method="get"><input class="searchBar search_youtube" name="search_query" type="text" placeholder="Youtube" /></form><form class="searchForm" action="https://en.wikipedia.org/w/index.php" method="get"><input class="searchBar search_wikipedia" name="search" type="text" placeholder="Wikipedia (en)" /></form></section>
<nav>
<ul class="buttonList">
<li class="button button_green"><a href="http://github.com/borisu0815">Github</a></li>
<li class="button button_grey"><a href="http://unapromisa.wordpress.com">Wordpress</a></li>
<li class="button button_grey buttonArrow"><a href="blog.naver.com/avrillinkin">La Casa de la Literatura</a>
<ul>
<li><a href="#">Works on NLP(Natural Language Processing)</a></li>
<li><a href="#">Essays on Literary Works</a></li>
<li><a href="#">Essays in Foreign Languages</a></li>
<li><a href="#">Toward A New Language</a></li>
</ul>
</li>
</ul>
<ul class="columnList">
<li class="column column_purple"><a>La Casa de la Musica</a>
<ul>
<li><a href="https://www.youtube.com/channel/UC0bFW1We8ZOYvqJL5CBjOFA">My Performance</a></li>
<li><a href="#">Writing on Music (and Machine)</a></li>
<li><a href="#/">Archive</a></li>
</ul>
</li>
<li class="column column_green"><a>La Casa de la Pintura</a>
<ul>
<li><a href="https://drive.google.com/drive/u/1/my-drive">Video Games</a></li>
<li><a href="https://drive.google.com/drive/u/1/my-drive">My List of Paintings</a></li>
<li><a href="https://drive.google.com/drive/u/1/my-drive">Paintings and Machine</a></li>
</ul>
</li>
<li class="column column_pink"><a>Etc</a>
<ul>
<li><a href="http://behindsciences.kaist.ac.kr">Behind Scineces (KAIST STP Magazine)</a></li>
<li><a href="http://stp.kaist.ac.kr/020302">Biography/CV</a></li>
<li><a href="https://www.sharelatex.com/project">Current Works</a></li>
<li><a href="mailto:borisu0815@gmail.com">Contact Me</a></li>
</ul>
script>
    var contactForm = document.querySelector('form'),
    inputEmail = contactForm.querySelector('[name="email"]'),
    textAreaMessage = contactForm.querySelector('[name="content"]'),
    sendButton = contactForm.querySelector('button');
    sendButton.addEventListener('click', function(event){
      event.preventDefault();
      sendButton.innerHTML = '{{ site.text.contact.ajax.sending }}';
      var xhr = new XMLHttpRequest();
      xhr.open('POST', '//formspree.io/{{ site.email }}', true);
      xhr.setRequestHeader("Accept", "application/json")
      xhr.setRequestHeader("Content-Type", "application/x-www-form-urlencoded")
      xhr.send(
        "email=" + inputEmail.value +
        "&message=" + textAreaMessage.value);
      xhr.onloadend = function (res) {
        if (res.target.status === 200){
          sendButton.innerHTML = '{{ site.text.contact.ajax.sent }}';
        }
        else {
          sendButton.innerHTML = '{{ site.text.contact.ajax.error }}';
        }
      }
    });
</script>



</li>
</ul>
</nav>
