# docs.rocket.chat

A portal for all Rocket.Chat projects' documentation and general contribution, structure and style guides.

## Site structure

Above all else, this portal strives to keep everything simple and easy to use.

Together Jekyll and GitLab pages offers the most supported and user friendly way for others to fork, edit, preview and contribute back without having to setup a local development environment just to write copy, add images and manage files.

Only use templates and includes when they are needed. Creating a template per page or splitting templates into many parts that are only included ones makes it challenging maintain and contribte to the project.

### Templates

The `default.html` template is the base template used by pages or other templates (only `post.html` at the moment).

Only create a template if it will be used by more than one page. Rather add the structure and content to the page e.g. see `index.html`.

### Includes

Like Templates, only create an Include if it will be used in more than one template.

### Styles

When changing styles bump the `version` number in `config.yml` to force browsers to load the new version.

Define template or page styles in their own file with the same name as the template or page and then add then include the style in `styles.scss`.

Only define variables for values that are used in multiple places and need to vary. Use contextually relevant names instead of calling it by the current value it holds e.g use `$body-color` instead of `$color-light-blue`. If you change the value of the variable in the second case to you have to update the name and  every where it is used.

### index.html

Lists Rocket.Chat projects defined in `/_data/projects.yml` and outlines how to contribute and links to contribution guides.

### news.html

WIP: Index page for all documentation news.

## Todo

- Design, UX and final CSS for portal
