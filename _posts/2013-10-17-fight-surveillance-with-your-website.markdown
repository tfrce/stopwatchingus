---
layout: post
title:  "Project Megaphone: <br />Fight Surveillance With 9 Lines of Code"
date:   2013-10-17 09:00:00
categories: 
---

<p style="font-size:19px; font-weight: bold; padding: 15px 0 0px 0">Own a website? We need your help.</p>

Mass surveillance is a threat to the Internet. The NSA's programs threaten our ability to communicate and conduct transactions privately online. This is a critical moment: If we don't convince Congress to make meaningful change Snowden's leaks have the public's attention, we may never have another chance.

That's why we, the EFF, ACLU, Free Press, Demand Progress, and dozens of other technology policy advocates have spent the last six weeks planning a rally in DC. 

<strong>We need to show Congress that passing meaningful legislation is critical.</strong>

All it takes to help is 9 lines of code. Add it to your personal blog or your company's website and our servers handle the rest. Everytime a visitor from cities nearby DC visits the site, we'll show them a banner advertising the rally.

### The code:

```
<!--[if gt IE 8]>
<script> 
  (function(){
    var e = document.createElement('script'); e.type='text/javascript'; e.async = true;
    e.src = document.location.protocol + '//d1ux67szpr7bp0.cloudfront.net/project-megaphone/widget.min.js';
    var s = document.getElementsByTagName('script')[0]; s.parentNode.insertBefore(e, s);
  })();
</script>
<![endif]-->
```

<h3 style="margin-bottom:15px">What the banner looks like:</h3>

See the default banner live on <a href="http://cdnjs.com" target="_blank">cdnjs</a> (geolcation is disabled).

You can also choose from three different banner designs. Check them out on our <a href="https://github.com/tfrce/project-megaphone" target="_blank">Github repo</a>.

<h3 style="margin-bottom:15px">Technical implementation:</h3>

Our geolocation service uses multiple load-balanced Rackspace servers, each of which runs a node.js-based IP geolocation service. Rackspace were kind enough to donate hosting for the project. The javascript itself is served via Cloudfront.

Some details on when the banner is served:

* The banner is only shown to users in areas within driving distance of DC. 
* Mobile users aren't shown the banner.
* The script automatically stops serving the banners at 12pm on October 26th (the start time of the rally)
* If a user closes the banner, it won't be shown to them again for 48 hours.


<h3 style="margin-bottom:15px">Why you, and specifically you, should take part:</h3>

Plato said that "the chief penalty [of good men who refuse to lead] is to be governed by someone worse." 

If you, the ones who create the content that's served on the Internet, don't act to defend it, who will?

