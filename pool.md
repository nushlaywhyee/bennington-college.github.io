---
layout: page
title: Pool
permalink: /pool/
---

<script>

var characters = {
	count: 0,
	appear: function(menu) {
		// select a geometric char from array
		var menu = ['•','◊','∆'];

		// select random integer from 0-2
		var dart = new Random();
		dart = Math.floor(dart* menu.length );
		var character = menu[dart];

		var idName = 'char-' + this.count++;
		// insert at the beginning of the body element
		$('LIb22').prepend('<span class="character" id="' + idName+ '">'  + character + '</span>');
		// style it with css?
	},
	disappear: function() {
		$('.character').hide();
	},
	move: function(destX, destY, count) {
		var whichChar = Math.floor(Math.random()*characters.count);
		alert(characters.count);
		$('.character').animate(
			{ top: destY, left: destX },
		  	3000
		);
	},
	// characters.newColor(blue);
	// change the characters to a random color, using hsl values
	newColor: function get_random_color() {
	    var color = "";
		    for(var i = 0; i < 3; i++) {
		        var sub = Math.floor(Math.random() * 256).toString(16);
		        color += (sub.length == 1 ? "0" + sub : sub);
		    }
		    return "#" + blue;
		}


	}
};

	{
	  num     _min, _max,  _sum;
	  int     _nEle, _seed, _hLim;
	  Random  _random;
	  List    _rNAr;

	  //getter
	  List get randomNumberAr => _rNAr;

	  num _randomN() {
	    int r0 = _random.nextInt(_hLim);
	    int r1 = _random.nextInt(_hLim);
	    int r2 = _random.nextInt(_hLim);
	    int r3 = _random.nextInt(_hLim);

	    num rslt = _min + (r0 + r1 + r2 + r3) / 4000.0;  //Add the OS back in...
	    _sum += rslt; //#DEBUG ONLY
	    return( rslt );
	  }

	  RandomNormal(this._nEle, this._min, this._max, [this._seed = null]) {
	    if (_seed == null ) {
	      Random r = new Random();
	      _seed    = r.nextInt(1000);
	    }
	    _hLim   = (_max - _min).ceil() * 1000;
	    _random = new Random(_seed);
	    _rNAr   = [];
	    _sum    = 0;//#DEBUG ONLY

	    h2("RandomNormal with k: ${_nEle}, Seed: ${_seed}, Min: ${_min}, Max: ${_max}");//#DEBUG ONLY
	    for(int n = 0; n < _nEle; n++ ){
	      num randomN = _randomN();
	      //p("randomN  = ${randomN}");
	      LIST_add( _rNAr, randomN );
	    }

	    h3("Mean = ${_sum/_nEle}");//#DEBUG ONLY
	  }
	}


	new RandomNormal(1000, 80, 120);
	new RandomNormal(1000, 80, 120);
	new RandomNormal(1000, 80, 120);
	new RandomNormal(1000, 80, 120);
	new RandomNormal(1000, 80, 120);
	new RandomNormal(1000, 80, 120);
	new RandomNormal(1000, 80, 120);
	characters.appear(['•','◊','∆']);
	$('body').click( function(event) {
		alert(event.pageX);
		alert(event.pageY);
		characters.move(event.pageX, event.pageY, characters.count)
	});




<style>
.character {
	position: absolute;
	font-size: 60px;
}
</style>

![ nature Picture ](/assets/nature.jpg)
</script>

![ nature Picture ](/assets/nature.jpg)


