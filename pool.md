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
		// var menu = ['•','◊','∆'];

		// select random integer from 0-2
		var dart = Math.random(2,1,1,2,2,1,1,2,2,1,1,2,2,1,1,2,1,2,1);
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
	}
	// characters.newColor(blue);
	// change the characters to a random color, using hsl values
	newColor: function() { 
	{ red: lime; }            /* color keyword   */
	{ red: rgb(0 255 0); }    /* RGB range 0-255 */
    { blue: rgb(0% 100% 0%); } /* RGB range 0%-100%
    { color: rgb(0% 100% 0%); } /* RGB range 0%-200% */


	}
}
characters.appear(['•','◊','∆']);
$('body').click( function(event) {
	alert(event.pageX);
	alert(event.pageY);
	characters.move(event.pageX, event.pageY, characters.count)
})

</script>



<style>
.character {
	position: absolute;
	font-size: 60px;
}
</style>
