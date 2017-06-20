# ghost-app-frontmatter

Ghost app to enable front matter on ghost posts

This app allow you to use frontmatter (yaml) in the post description, then you could access to extra data in the property data of the post

## Example

You can use front matter using the `+++` delimiter

```markdown
+++
blurb: 'Awesome Data'
link: 'http://google.ca'
+++

# My Blog Post

Front matter is awesome
```

Then you could use the `data`property of the post object in yours template

post.hbs
```handlebars
{{#if data.link}}
	<a href="{{data.link}}">{{title}}</a>
{{/if}}

<div>{{data.blurb}}</div>
```

## Installation

### Manual Installation

1. Download this repo
2. Copy the folder: `ghost-app-frontmatter` to your Ghost apps folder: `content/apps/ghost-app-frontmatter`
3. Update your Ghost blog's `activeApps` to include the app: `"key":"activeApps","value":"["ghost-app-frontmatter"]"`

For details on how to modify your database, see: [Getting Started: Installing](https://github.com/TryGhost/Ghost/wiki/Apps-Getting-Started-for-Ghost-Devs#installing)
