---
layout: main
---

# Embedded Component Examples

### Here's an embedded component (`Greeter.svelte`)

{% embedSvelte 'Greeter.svelte', { name: 'Zach' } %}



---

## _Interesting notes on the output code_

- Although the same component is embedded here twice (`Greeter.svelte`), the component's source code is only generated _once_ (as is necessary).
- Two Svelte components exist on this page, but the Svelte utility code exists _only once_. This is because all Svelte code for a single page is built in a **single** Rollup build, which allows Rollup to properly de-dupe and tree-shake the code. No unnecessary code bloating up the page.
