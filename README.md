# Search Bar

You're an engineer here at AngelList. We've decided to iterate on the job search experience for candidates. You've been tasked with prototyping a simple search bar for candidates to filter jobs by role (e.g. engineer, designer).

Here are the mocks you've been given:

<img src="mock.png" width="700" />
<img src="expanded.png" width="700" />

You'll be using vanilla JavaScript (no frameworks), HTML, and CSS to build this search bar.

Your code should:
- Make a `GET` request to `/roles` retrieve the list of role options.
- Create the dropdown with the options formatted as depicted in the mock.
- When the Search button is clicked, make a `POST` request to `/search` with a payload of `{ roleId }`.
- Style the UI according to the mocks.

You'll write everything in the Coderpad. You'll see that there's a designated section for CSS, one for HTML, and one for JavaScript.

**Feel free to look anything up online.**

### How to make API requests

We've provided an `api` function for you to use. It takes an HTTP method and path to request, and an optional data argument (if you are making a `POST` request). The `api` function will return a promise that may have data. It can also potentially reject with an error.

```typescript
api(method: string, path: string, data?: any): Promise<any>
```

### Design specs

- All text is 16px
- All corners are rounded by 5px
- Colors: `#f2f4f7` (light gray background), `#0f6fff` (blue), `#acbdd5` (select border)
- Just eyeball everything else. No need to be pixel perfect -- remember, this is a prototype!
- Style the select last. The svg for the background indicator is here: https://cl.ly/84375e17a5e9/arrow-down.svg
