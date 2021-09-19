# search SuperHero and make them favorite
## usage
1. click [here](https://wizzenalum.github.io/search-super-hero/) 
2. now you just type your favorite superhero name and hit enter or click on search.
3. you can superhero your favorite
4. To know more about the super hero click more.
5. that's it.....  

## For developers
> To know in depth about this, you can visit my [youtube](wizzenalum.com).
> Recreation of the application will need vanila javascript, html, css only also need to create the token number to use [superhero-Api](https://www.superheroapi.com/).

## Folder structure

It has minimilistic folder structure with entry point index.html.

> ├── README.md \
> ├── index.html \
> ├── script \
> │ ├── Component.js \
> │ └── index.js \
> └── style \
> └── style.css \

## File wise code

actually index.html only has metadata and links to connect to css and script. so all the html will be created during the runing the web application using javascript.

1. render() will render the UI as the states changes by any events and most of code for rendering the deferrent views are in the Component.js. there is three views home, favorite and hero.
2. index.js has states that decides the current view by currentWindow variable and other data shown in the page by defferent other variables of the object state.
3. index.js also hase all the event listeners with eventlistner controller (manageEvents) that set listners according to the current view.
4. index.js also manage the api call as user search.
5. css is minimilist but enough to make presentable.

## Code flow

here i am showing how all function call going to happen with the user intrect with the GUI.

- What happen each time

```sh
index.html--> render()-->rootComponent() it call view specific function --> manageListenrs() it set listeners according to the view.
```

- initial loading of the web application

```sh
render()--> rootComponent(state)--> setSearchComponent(state)--> createList(list,home)--> manageListenrs()--> rootListeners()-->searchlistners()
```

- when user click to search for superhero

```sh
handleSearchClick()--> handleXMLRequest()--> here new state is set --> render()--> rootComponent(state)--> setSearchComponent(state)--> createList(list,home)--> manageListenrs()--> rootListeners()-->searchlistners()
```
