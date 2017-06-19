# ghost-app-frontmatter

Ghost app to enable front matter on ghost posts

This app allow you to use frontmatter (yaml) in the post description, then you could access to extra data in the property data of the post

## Example

You can use front matter using the `+++` delimiter

```markdown
+++
blurg: 'Awesome Data'
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
