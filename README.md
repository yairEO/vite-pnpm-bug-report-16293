# Vite bug report - test case

Regarding issue https://github.com/vitejs/vite/issues/16293

This happens with using `pnpm` only. Verified to be working using `npm` (which I never use cause it sucks)

Note that this repo already includes a 3rd-party highly-simplified module in `node_modules`.

Simply run `pnpm i` then `pnpm dev` and open the served app on the browser and view the error in the console:

![image](https://github.com/yairEO/vite-pnpm-bug-report-16293/assets/845031/8d34c604-3b5b-47cc-ba20-cc97e09eb9b0)

> Uncaught SyntaxError: The requested module '/node_modules/.pnpm/react-dom@18.2.0_react@18.2.0/node_modules/react-dom/server.browser.js?v=60c0bbfc' does not provide an export named 'renderToStaticMarkup'

---

I came across this bug when trying to locally test my [Tagify](https://github.com/yairEO/tagify/) component by creating the most basic `Vite` project and importing Tagify as a (local file) dependency. 
