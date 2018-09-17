# Temp Repo for ticket https://github.com/rollup/rollup/issues/2461

- Rollup Version: 0.66
- Operating System (or Browser): MacOS High Sierra 10.13.6 (17G65) / Google Chrome 68.0.3440.106 (Official Build) (64-bit)
- Node Version: 8.1.0

### How Do We Reproduce?

This is Sapper specific, so a little hard to reproduce without a Sapper setup. So I set up a temporary repo like so for install:

```bash
git clone https://github.com/arxpoetica/rollup-ticket.git
cd rollup-ticket
npm install
npm run dev
```

Then go to http://localhost:3000 and see the following:

### Expected Behavior

The CSS in the `<Popup.../>` component should show up (red background, white text).

### Actual Behavior

The CSS does not show up.

To get the CSS to show, do either of the following:

* In the main `routes/index.html` file, remove or comment out line 10: `// import debounce from './debounce.js'`

or

* In the `routes/alt.html` file, remove or comment out lines 3 and 8: `<!-- <Popup message="This is a block of text. Notice, the text always shows up, but not always the CSS styles."/> -->` and `// Popup: '../components/Popup.html'`
