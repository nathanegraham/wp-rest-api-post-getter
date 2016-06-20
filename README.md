# Get WP Posts Using REST API and Javascript

###Overview

The files in this repository can be used to display posts using the WP REST API from a WordPress site on an external site. You can see a minimalist demo on this approach on [my site](http://nathanegraham.github.io/).

###What It Does

* Gets a thumbnail of the featured media associated with the post (if present)
* Gets the post title
* Adds link to the post title that takes user to post on WP site
* Gets the creation date of the post
* Gets the post excerpt
* Lists most recent 2 posts
* Has Show More button that allows user to click and see next 2 posts and so forth

###How to Use It

1. Activate the [WP REST API v2 plugin](https://wordpress.org/plugins/rest-api/) on the WP site
2. Download or clone this repository
2. Open script.js in your favorite editor
3. On line 2, copy and paste the domain for the WP site you want to get posts from and add "/forms/wp-json/wp/v2" to the path like this
'''javascript
var endpoint = "https://yourdomain.com/forms/wp-json/wp/v2",
'''
4. Upload the three Javascript files to your external site
5. Copy the relevant HTML and paste it into your template page(s)
6. Add styles and reorganize as needed

###Tips

* To change the number of posts that display, **open script.js** and change the value on **line 3**. For example, this shows 2 posts:
'''javascript
itemsPerPage = 2,
'''
* Delete this line to remove the loading message
'''
<div class="loading" v-show="loading">loading...</div>
'''
