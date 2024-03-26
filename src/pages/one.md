# how to use layout in other components

Once the template (layout component) is created, you can import it into your components. Then, wrap the content within the layout component. This content will be injected into the slot component in the layout.

```
<BaseLayout title={frontmatter.title} fancyJsHelper={fancyJsHelper}>
  Welcome to my new Astro blog, using MDX!
</BaseLayout>
```

layout

```
---
const { title, fancyJsHelper } = Astro.props;
---
<!-- -->
<h1>{title}</h1>
<slot /> <!-- your content is injected here -->
<p>{fancyJsHelper()}</p>
<!-- -->
```
