# Using Svelte directly with Vite

No svelte*kit*

## What we want

* Basic svelte

* Svelte version 5

* New rune syntax - dollar syntax
    ```javascript
        let count   =  $state(0)
        let doubled =  $derived(count * 2);        
    ```  
    [Docs](https://svelte.dev/docs/svelte/$derived)

* Export compiled components,
  so we can use them inside any HTML context



```bash
npm create vite@latest 
#  select "my-project-name"
#  choose svelte 

cd  my-project-name
npm install


# original README.md renamed to readme-scaffold.md


# start dev server
npm run dev
# start dev server and open the app in a new browser tab
npm run dev -- --open

# production version of your app:
npm run build

# preview the production build with
npm run preview

```

## App structure

* `index.html`  
    the outer HTML 

* `./src/main.ts`   
    * adapter
    * imports and instantiates `./src/App.svelte`
    * dont change

* `./src/App.svelte`
    * body content
    * imports and  instantiates components from `./src/lib/ChatCompletion.svelte`


* static assets in ./public  
    for example vite.svg

* static assets in ./src/  
    for example app.css

* static assets in ./src/assets  
    for example svelte.svg



