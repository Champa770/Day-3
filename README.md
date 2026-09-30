# Day-3
Images and Tables
**Images — the `<img>` tag**

```html
<img src="cat.jpg" alt="A sleeping cat">
```

`<img>` is a void element — no closing tag, no content between tags.

- `src` — path to the image file (required)
- `alt` — text shown if the image fails to load, and read aloud by screen readers (required for accessibility, don't skip it)

**Image paths**

```html
<img src="images/cat.jpg" alt="Cat">        <!-- relative path, same project -->
<img src="https://example.com/cat.jpg" alt="Cat">  <!-- absolute/external URL -->
```

Relative path = image lives inside your own project folder. Absolute URL = image is hosted elsewhere.

**Controlling size**

```html
<img src="cat.jpg" alt="Cat" width="300" height="200">
```

Width/height here are in pixels. Better practice (mention briefly, not deep dive — that's CSS territory): sizing is usually done with CSS later, not these attributes, but good to know they exist.

**Other useful image-related attributes**

```html
<img src="cat.jpg" alt="Cat" title="Hover text appears here">
```

`title` shows a tooltip on hover — different from `alt`, which is for accessibility/fallback.

**Figure and caption (semantic pairing for images)**

```html
<figure>
  <img src="cat.jpg" alt="A cat sleeping on a couch">
  <figcaption>My cat, Whiskers, napping.</figcaption>
</figure>
```

Use this when an image needs a caption — keeps image + caption semantically grouped.

---

**Tables — structure**
Tables are for tabular data (rows and columns) — not for page layout (that was an old, bad practice).

```html
<table>
  <tr>
    <th>Name</th>
    <th>Age</th>
  </tr>
  <tr>
    <td>Mohit</td>
    <td>22</td>
  </tr>
  <tr>
    <td>Riya</td>
    <td>21</td>
  </tr>
</table>
```

- `<table>` — wraps the whole table
- `<tr>` — table row
- `<th>` — table header cell (bold, centered by default)
- `<td>` — table data cell (regular content)

**Better structure using thead/tbody**

```html
<table>
  <thead>
    <tr>
      <th>Name</th>
      <th>Age</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Mohit</td>
      <td>22</td>
    </tr>
  </tbody>
</table>
```

`<thead>` groups header rows, `<tbody>` groups body rows. Not required for a table to work, but it's the standard/clean way to write one, especially once styling comes in.

**Merging cells**

```html
<table>
  <tr>
    <th colspan="2">Student Info</th>
  </tr>
  <tr>
    <td>Mohit</td>
    <td>22</td>
  </tr>
</table>
```

`colspan` — merges cells across columns. `rowspan` — merges cells across rows (same idea, vertical).

**Common mistakes**

- Missing `alt` on images
- Using tables for page layout instead of actual tabular data
- Forgetting `<tr>` around `<td>`s — cells floating without a row wrapper breaks the table
- Mismatched number of `<td>`s per row, making columns misalign

**Small practice task**
Build a page with:

- An image using `<figure>` + `<figcaption>`
- A table listing 3 students with Name, Age, and Grade columns
- One header row using `<th>`, using `colspan` for a title row above it
