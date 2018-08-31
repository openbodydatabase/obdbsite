+++
title = "Subscribe for updates"
menuname = "Subscribe"
weight = 60
draft = false
+++

<form id="contactform" method="post" action="https://formspree.io/contact@obdb.org">
	<div class="field half first">
		<input type="text" name="name" id="name" placeholder="Name"/>
	</div>
	<div class="field half">
		<input type="email" id="email" name="email" placeholder="Email">
	</div>
	<ul class="actions">
		<li><input type="submit" value="Send message" class="special" /></li>
		<li><input type="reset" value="Reset" /></li>
	</ul>
	<input type="hidden" name="_next" value="#thankyou" />
	<input type="hidden" name="_subject" value="Contact form entry" />
	<input type="text" name="_gotcha" style="display:none" />
</form>

<script>
$(document).ready(function($) {
    $(function(){
        if (window.location.search == "#thankyou") {
        	$('#contactform').hide();
        	$('#contactformsent').show();
        } else {
        	$('#contactformsent').hide();
        }
    });
});
</script>
