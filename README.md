# Rowat Insurance

**Welcome, seoplus+**

Before making any changes to site files, always start your task by doing a `git pull`, and end by doing a `git push`, so that you are working with the latest version of the site files and won't have any merge conflicts with the changes I am making on my end simultaneously.

## This site was built using static site builder Jekyll

If you would like to see a development preview of your changes, you will need both [Ruby v.2.3+](https://www.ruby-lang.org/en/documentation/installation/) and [Jekyll v.3.5+](https://jekyllrb.com/) installed on your machine. Then you can serve the files with `jekyll serve` in your terminal, and navigate to localhost:4000 on your browser. Both the development and the production files are served out of the `_site` folder, which is generated on `jekyll serve` or `jekyll build` commands.  Changes made by you to anything in the` _site` folder directly will be overwritten, so always be sure you are editing files outside of the `_site` folder.

If you would like to push your changes live without previewing the build with `jekyll serve`, you may simply commit your changes and push to GitHub.

All changes pushed to the GitHub repository will trigger a production build automatically and deploy the contents of the newly built `_site` file to the server.  The changes should be live within 5 minutes.  If ever your changes fail to propagate, [email me](mailto:pamelasusanhicks@gmail.com) so that I can trigger a deploy manually and check the error log for problems.

## Editing content

Jekyll is a template compiler, so many of the site components are extracted to separate files for ease of development:
1. Pages are in the `_pages` folder, except the `index.html`, which is on the root.
2. The head, header, footer, and other components are in the `_includes` folder.
3. JSON-LD schema is in the `_includes/schema` folder ('organization' appears on the English-language homepage only, 'insurance-agency' appears on every page except blog posts, and 'blog-post' appears on every post).
4. Global data and configurations are in the `_config.yml` file on the root.
5. Multilingual text has been extracted to the `lang.yml` file in the `_data` folder.

### Edit metadata

All titles and meta description tags (metadata) is contained within YAML front matter [see an example](https://jekyllrb.com/docs/frontmatter/).

Default metadata that will appear on any pages without its own metadata is set in the `_config.yml` (item 4 above).

Every other page (item 1 above) has its metadata set in its YAML front matter, where `title: ` is the title, and `excerpt: ` is the description. Blog posts are set to use the post title and the excerpt as its metadata automatically.

Don't forget to use html characters instead of symbols (e.g., `&amp;` instead of "&amp;", `&#39;` instead of " &#39; ", etc.) as symbols can break Jekyll.

### Publish blog posts

The blog posting interface can be accessed at [https://rowatinsurance.com/admin](https://rowatinsurance.com/admin).


#### Collections page (/admin/#/collections/blog)

In the menu on the left, click the + to create a new post. 

From the post editor (/admin/#/collections/blog/entries/new), you can create a new post.

**Notes:**
- All fields are required.
- You may compose the body  of the post in rich text or toggle Markdown if Markdown is more your thing.
- Your image should be at least 1280px wide.
- Category options are static.  If you would like me to add a category, [let me know](mailto:pamelasusanhicks@gmail.com)!
- I have disabled the option to review drafts before publishing; when you click 'Save', you are publishing to the repo, which triggers a build to the live site.

#### Bilingual posts

If you publish the post in English only, the post will appear in the site's blogroll (/blog/) as usual, however there will not be a Français link in the header or footer of the post, and the post will not appear in the French blogroll (/fr/blog/).

If you choose to publish the post in French as well, choose 'Français' from the language dropdown in the post editor, and use the *exact same* image as was used for the English version of the post. The image path is the reference that connects a French post to its English version so that the alternate language option appears in the header and footer of the post page.
