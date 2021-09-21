# SuperHero search engine UI
## Usage
1. Visit the application. HyperLink given at fifth point.
2. Now, you just type your favorite superhero name and hit enter or click on search.
3. You can  add superheros to  your favorite list.
4. To know more about the super hero click more.
5. That's it..... NOW, visit [here](https://wizzenalum.github.io/search-super-hero/) 

## For developers
> To know in depth about this application, you can visit my [youtube-video](https://youtu.be/e4N5PMvieXs). \
> Recreation of the application will need vanila javascript, html, css only also need to create the token number to use [superhero-Api](https://www.superheroapi.com/).

## Folder structure

It has minimilistic folder structure with entry point index.html.

> ├── README.md \
> ├── index.html \
> ├── script \
> │ ├── Component.js \
> │ └── index.js \
> └── style \
>     └── style.css

## File wise code

Actually index.html only has metadata and links to connect to css and script. so all the html will be created during the runtime of application using javascript.

1. render() will render the UI as the states changes by any events and most of code for rendering the deferrent views are in the Component.js. there is three views home, favorite and hero.
2. index.js has states that decides the current view by currentWindow variable and other data shown in the page by defferent other variables of the object state.
3. index.js also hase all the event listeners with eventlistner controller (manageEvents) that set listners according to the current view.
4. index.js also manage the api call as user search.
5. css is minimilist but enough to make presentable.

## Code flow

Here you can see how all function-calls going to exicute, when the user intrect with the GUI.

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
