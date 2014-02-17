#Anchorcms image upload fix

Anchorcms: 0.9.1 + 0.9.2   


##Installation
####Care if you have modified files:
new: anchor/libraries/uploader.php  
replace: anchor/views/assets/js/dragdrop.js  
replace: anchor/routes/posts.php

####Setup
1. Download the files.
2. Unzip the files and upload it to your Anchorcms installation.
3. Clear your browser cache.
4. Now you can upload an image with drag&drop it into the post editor.
5. Have fun with blogging =)

###Problems
If you upload an image and the link is like

```![image1.jpg](//content/image1.jpg)```


edit the **anchor/routes/posts.php** on line **263**

from:
<pre>
$uri = Config::app('url', '/') . '/content/' . basename($filepath);
</pre>

to:

<pre>
$uri = Config::app('url', '/') . 'content/' . basename($filepath);       
</pre>





Thanks to [tovic](http://forums.anchorcms.com/profiles/tovic)