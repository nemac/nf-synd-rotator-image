News/Features Syndicated News Rotator Image

The files in this project document a procedure for adding a default
image to the News/Features Syndicated News content type (machine-name
"news").

This git project exists simply to document the steps; this isn't a
Drupal module or anything else that needs to be installed on the site.

1. The first thing that needs to be done is to modify some CSS that is
   part of the site theme and which seems to interfere with the
   correct layout for "news" content items in teaser form.  In
   particular, the following two rules in the file
   `sites/all/themes/custom/mu/css/mu-alpha-default.css` need to be
   commented out:

   ```css
   .view-nf-front-page-departments .node-news.view-mode-tiny_teaser .group-right {
       width:100%;
   }
   ```

   ```css
   .view-nf-front-page-departments .node-news.view-mode-tiny_teaser .group-left {
       width:0;
   }
   ```
