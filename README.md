# minima-improved
Jekyll's Minima theme, with add-ons and powerups.

This README will only list the improvements made upon the base Minima theme. Visit https://github.com/jekyll/minima to the get full documentation on Minima.

## Improvements

- Support Goodreads among the social links.
- Render tags for posts, both in the list of posts and in the post page.
- Support links to canonical posts in case the post is originally posted somewhere else and this blog contains a copy of it. To use this feature you need to add information regarding the canonical post to your post's front-matter, e.g.
  
  ```yaml
  canonical_url: 'https://neptune.ai/blog/machine-learning-model-management-in-2020-and-beyond'
  remote_blog: 'neptune.ai'
  ```
- Lets you list some selected showcased posts in the homepage instead of all posts. To enable this, add the following to `_config.yaml`
  
  ```yaml
  minima:
    showcase_posts: true
  ```
  When enabled, the home page will only list the posts having `showcase: true` in their front-matter.

- Adds archive pages for tags using the jekyll-archive plugin. To enable, install the plugin and then add the following to your `_config.yaml`
  ```yaml
  jekyll-archives:
    enabled: ['tags']
    layout: archive
    permalinks:
      tag: '/archive/tag/:name/'
  ```
  After this is added, `/archive/tag/some-tag` will list all the posts having that tag.
