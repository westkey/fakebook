<h1>Facebook comment generator</h1>
<p>
  Hand tailored, copy/paste solution with CDN dependencies. 
  The links might break at some point, but who cares! Avatars and last names are fetched with faker.js. To prevent gender       issues I hardcoded some "gender neutral" first names (they are not perfect). Have fun! FOR EDUCATIONAL PURPOSES ONLY. 
</p>
<h2>Usage</h2>

    <div id="comments" style="width: 600px; background: white;"></div>
    <script>
    	var myComments = [
    		"This is awesome!",
    		"I'm so glad I bought this bullshit product.",
    		"This totally changed my life for the better. Thank you so much! How can I donate?"
    	];
    	(function load() {
    		var _fakebook = document.createElement("script");
    		_fakebook.src = "https://cdn.rawgit.com/vuoriov4/fakebook/master/fakebook.js";
    		document.head.appendChild(_fakebook);
    		_fakebook.onload = function() {
    			var _faker = document.createElement("script");
    		    _faker.src = "https://cdn.rawgit.com/Marak/faker.js/master/build/build/faker.min.js";
    		    document.head.appendChild(_faker);
    			_faker.onload = function() {
    				document.getElementById("comments").innerHTML = fakebook.generate(myComments);
    			};
    		}
    	})();
    </script>
    
<img src="preview.jpg"/>
