# Job Filter

You're an engineer here at AngelList. We've decided to iterate on the job search experience for candidates. You've been tasked with prototyping a simple job filter for candidates to look for jobs by role (e.g. engineer, designer).

Here are the mocks you've been given:

<img src="mock.png" width="700" />
<img src="expanded.png" width="700" />

You'll be using vanilla JavaScript (**no frameworks**), HTML, and CSS to build this job filter.

Your code should:
- Make a `GET` request to `/roles` retrieve the list of role options.
- Create the dropdown with the options formatted as depicted in the mock.
- When the Search button is clicked, make a `POST` request to `/search` with a payload of the shape:
```javascript
  {
    type: 'role',
    meta: {
      id: roleId
    }
  }
```
- Style the UI according to the mocks.

You'll write everything in the Coderpad. You'll see that there's a designated section for CSS, one for HTML, and one for JavaScript.

**Feel free to look anything up online.**

### How to make API requests

We've provided an `api` function for you to use; it will be available in scope of your JavaScript. `api` takes an HTTP method and path to request, and an optional data argument (if you are making a `POST`). The function will return a promise that may have data. It can also potentially reject with an error.

```typescript
api(method: string, path: string, data?: any): Promise<any>
```

### Design specs

- All text is 16px
- All corners are rounded by 5px
- Colors: `#f2f4f7` (light gray background), `#0f6fff` (blue), `#acbdd5` (gray select border)
- SVG for the `<select>` down arrow: [https://tiffwu.github.io/job-filter/arrow-down.svg](https://tiffwu.github.io/job-filter/arrow-down.svg)
- Just eyeball everything else. No need to be pixel perfect -- remember, this is a prototype!

### Hints

#### Select styling
<details>
  <summary>Click to expand</summary>

  A stylesheet is provided to help with styling the `<select>` element: [https://tiffwu.github.io/job-filter/style.css](https://tiffwu.github.io/job-filter/style.css). Import this stylesheet into the page before doing the remainder of the styling. Feel free to look at the contents of the CSS file.
</details>
