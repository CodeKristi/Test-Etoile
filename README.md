
## First of All I Would like to Thank You for Your Purchase, You Are Awesome!

### Documentation

Product documentation is available online [https://docs.unbound.studio/etoile-writer-blogger-jekyll-theme]
(https://docs.unbound.studio/etoile-writer-blogger-jekyll-theme).

<!--
TO DO:
* _drafts folder (save files without date) - DONE
* add about page & link in navigation - DONE
* ordering of post files within _posts folder
* remove / hide authors folder / files / references
* Home: keep "about me" section there
* Home: divide posts into categories to display instead of list of latest (use "spotlight" section for latest, followed by different categories)
* "ask me" page with FAQs??
* Contact: add spotlight section under contact form
* Nav bar - add "home" logo instead of word
* Blog page: have related posts below blog post & recent posts in sidebar
* Style opened nav search bar for mobile view (navbar.scss)
 -->

<!-- http://127.0.0.1:4000
bundle exec jekyll s -->

<!--
* "page" refers to the page you're on and its front matter variables, or to the "page" variable from the layout that's being used
*
-------------------------------------------------------------------------------
FOLDER STRUCTURES & SITE LAYOUT
-------------------------------------------------------------------------------
"HOME" PAGE VISIBLE LAYOUT
a) Inside default.html file (contained within _layouts folder)
    ~ head.html
        ~~ (site brand image)
        ~~ head-custom.html
        ~~ google-analytics.html
    ~ header.html
        ~~ (site logo) (site title)
        ~~ navbar-primary.html
            ~~~ (search)
            ~~~ social-networks.html
            ~~~ donations-paypal.html
    ~ (CONTENT) - refers to index.md file
    ~ footer.html
        ~~ widget-(xxx).html
            ~~~ (logo, title, description, copyright)
            ~~~ social-networks.html
    ~ offcanvas.html
        ~~ social-networks.html (social icons on left / bottom of pages)
b) Inside index.md file
    * layout: full (= layout: default)
    ~ section-ad.html (adverts section #1)
    ~ section-featured.html
        ~~ content-media-left-1-2.html (50% page division with media on left)
    ~ section-spotlight.html
        ~~ content-media-top.html (3 columns in full width with media on top)
    ~ section-mailchimp.html
    ~ section-latest.html
        ~~ content-media-left-1-3.html (30%-60% page division with media on left)
    ~ section-ad.html (adverts section #2)
    ~ section-authors.html (multiple authors)
        ~~ content-author.html
    ~ section-instagram.html
    ~ section-cta.html
    ~ section-author.html (singular author)
        ~~ author.html

================================================================================

"ALL POSTS (and) PAGES > BLOG" PAGE VISIBLE LAYOUT
a) Inside default.html file (contained within _layouts folder)
    ~ head.html
        ~~ (site brand image)
        ~~ head-custom.html
        ~~ google-analytics.html
    ~ header.html
        ~~ (site logo) (site title)
        ~~ navbar-primary.html
            ~~~ (search)
            ~~~ social-networks.html
            ~~~ donations-paypal.html
    ~ (CONTENT) - refers to index.html (contained within "blog" folder)
    ~ footer.html
        ~~ widget-(xxx).html
            ~~~ (logo, title, description, copyright)
            ~~~ social-networks.html
    ~ offcanvas.html
        ~~ social-networks.html (social icons on left / bottom of pages)
b) Inside index.html file (contained within "blog" folder)
    * layout: default
    ~ section-featured.html ("featured" title removed)
        ~~ content-media-left-1-2.html (50% page division with media on left)
    ~ content-media-left-1-3.html (30%-60% page division with media on left)
    ~ paginate-blog.html (reference jekyll-paginate package)
    ~ section-spotlight.html
        ~~ content-media-top.html (3 columns in full width with media on top)

Front matter variables
_______________________
title: Best tech companies to work for in 2019
image: post-image.jpg       # Upload the image to uploads directory
categories: [business]      # Same as category post tag
tag: [spotlight, featured]  # Optional: spotlight tag adds post to spotlight section, featured tag add post to featured section
hidden: true                # Optional: exlude the post from blog page posts
author: sarah               # Reference author username

================================================================================

"BUSINESS / CULTURE /TRAVEL /SPORT" PAGE VISIBLE LAYOUT
a) Inside default.html file (contained within _layouts folder)
    ~ head.html
        ~~ (site brand image)
        ~~ head-custom.html
        ~~ google-analytics.html
    ~ header.html
        ~~ (site logo) (site title)
        ~~ navbar-primary.html
            ~~~ (search)
            ~~~ social-networks.html
            ~~~ donations-paypal.html
    ~ (CONTENT) - refers to category.html (contained within _layouts folder)
    ~ footer.html
        ~~ widget-(xxx).html
            ~~~ (logo, title, description, copyright)
            ~~~ social-networks.html
    ~ offcanvas.html
        ~~ social-networks.html (social icons on left / bottom of pages)
b) Inside category.html (contained within _layouts folder)
    * layout: default
    ~ (page.tag used as title)
    ~ content-media-left-1-2.html (50% page division with media on left) (first post in category)
    ~ content-media-left-1-3.html (30%-60% page division with media on left) (more posts in category)
    ~ section-spotlight.html
        ~~ content-media-top.html (3 columns in full width with media on top)
    ** add paginate-blog.html ??
    ** check the contents displayed in spotlight (don't display same contents twice)

================================================================================

"PAGES > CONTACT" PAGE VISIBLE LAYOUT
* Page built using page.html file, based on default.html
a) Inside default.html file (contained within _layouts folder)
    ~ head.html
        ~~ (site brand image)
        ~~ head-custom.html
        ~~ google-analytics.html
    ~ header.html
        ~~ (site logo) (site title)
        ~~ navbar-primary.html
            ~~~ (search)
            ~~~ social-networks.html
            ~~~ donations-paypal.html
    ~ (CONTENT) - refers to page.html (contained within _layouts folder)
    ~ footer.html
        ~~ widget-(xxx).html
            ~~~ (logo, title, description, copyright)
            ~~~ social-networks.html
    ~ offcanvas.html
        ~~ social-networks.html (social icons on left / bottom of pages)
b) Inside page.html (contained within _layouts folder)
    * layout: default
    ~ (title)
    ~ (CONTENT) - refers to contact.md (main content on page, no sidebar)
    ~ sidebar-page.html (sidebar widgets on page - not displayed)
c) Inside contact.md file
    ~ formspree.html
    * reference to "thanks.md" file

================================================================================

"PAGES > SIDEBAR LEFT" PAGE VISIBLE LAYOUT
* Page built using page.html file, based on default.html
a) Inside default.html file (contained within _layouts folder)
    ~ head.html
        ~~ (site brand image)
        ~~ head-custom.html
        ~~ google-analytics.html
    ~ header.html
        ~~ (site logo) (site title)
        ~~ navbar-primary.html
            ~~~ (search)
            ~~~ social-networks.html
            ~~~ donations-paypal.html
    ~ (CONTENT) - refers to page.html (contained within _layouts folder)
    ~ footer.html
        ~~ widget-(xxx).html
            ~~~ (logo, title, description, copyright)
            ~~~ social-networks.html
    ~ offcanvas.html
        ~~ social-networks.html (social icons on left / bottom of pages)
b) Inside page.html (contained within _layouts folder)
    * layout: default
    ~ (title)
    ~ (CONTENT) - refers to sidebar-left.md (main content on page)
    ~ sidebar-page.html (sidebar widgets on page)
c) Inside sidebar-left.md file
    ~ (text)

================================================================================

"PAGES > SIDEBAR RIGHT" PAGE VISIBLE LAYOUT
* Page built using page.html file, based on default.html
a) Inside default.html file (contained within _layouts folder)
    ~ head.html
        ~~ (site brand image)
        ~~ head-custom.html
        ~~ google-analytics.html
    ~ header.html
        ~~ (site logo) (site title)
        ~~ navbar-primary.html
            ~~~ (search)
            ~~~ social-networks.html
            ~~~ donations-paypal.html
    ~ (CONTENT) - refers to page.html (contained within _layouts folder)
    ~ footer.html
        ~~ widget-(xxx).html
            ~~~ (logo, title, description, copyright)
            ~~~ social-networks.html
    ~ offcanvas.html
        ~~ social-networks.html (social icons on left / bottom of pages)
b) Inside page.html (contained within _layouts folder)
    * layout: default
    ~ (title)
    ~ (CONTENT) - refers to sidebar-right.md (main content on page)
    ~ sidebar-page.html (sidebar widgets on page)
c) Inside sidebar-right.md file
    ~ (text)

================================================================================

"PAGES > 404" PAGE VISIBLE LAYOUT
* Page built using 404.html file, based on default.html
a) Inside default.html file (contained within _layouts folder)
    ~ head.html
        ~~ (site brand image)
        ~~ head-custom.html
        ~~ google-analytics.html
    ~ header.html
        ~~ (site logo) (site title)
        ~~ navbar-primary.html
            ~~~ (search)
            ~~~ social-networks.html
            ~~~ donations-paypal.html
    ~ (CONTENT) - refers to 404.html (contained within _layouts folder)
    ~ footer.html
        ~~ widget-(xxx).html
            ~~~ (logo, title, description, copyright)
            ~~~ social-networks.html
    ~ offcanvas.html
        ~~ social-networks.html (social icons on left / bottom of pages)
b) Inside 404.html (contained within _layouts folder)
    * layout: default
    ~ (title)
    ~ (CONTENT) - refers to 404.md (main content on page)
c) Inside 404.md file
    ~ (image)
    ~ (text)

================================================================================

"AUTHORS > name" PAGE VISIBLE LAYOUT
* Page built using author.html file, based on default.html
a) Inside default.html file (contained within _layouts folder)
    ~ head.html
        ~~ (site brand image)
        ~~ head-custom.html
        ~~ google-analytics.html
    ~ header.html
        ~~ (site logo) (site title)
        ~~ navbar-primary.html
            ~~~ (search)
            ~~~ social-networks.html
            ~~~ donations-paypal.html
    ~ (CONTENT) - refers to author.html (contained within _layouts folder)
    ~ footer.html
        ~~ widget-(xxx).html
            ~~~ (logo, title, description, copyright)
            ~~~ social-networks.html
    ~ offcanvas.html
        ~~ social-networks.html (social icons on left / bottom of pages)
b) Inside author.html (contained within _layouts folder)
    * layout: default
    ~ (image, title, bio)
    ~ (CONTENT) - refers to (author-name).md (contained in _authors folder)
    ~ (social media)
    ~ content-media-left-1-3.html (with author's articles)
    ~ paginate-blog.html (reference jekyll-paginate package)
c) Inside (author-name).md file
    ~ (front matter tags)
    ~ (text)

-------------------------------------------------------------------------------

NAVIGATION & WIDGETS CONTENT
Inside the _data folder

AUTHORS BIO'S
Inside the _authors folder

CATEGORIES (referenced in category.html)
Inside the _category folder

 -->
