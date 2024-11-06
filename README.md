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


# development 
npm run dev

# production version of your app:
npm run build

# preview the production build with
npm run preview




```