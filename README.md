### hyperapp
---
https://github.com/jorgebucaran/hyperapp

```js
import { h, app } from "hyperapp"
const state = {
  count: 0
}
const actions = {
  down: value => state => ({ count: state.count - value }),
  up: value => state => ({ count: state.count + value })
}
const view = (state, actions) => (
  <div>
    <h1>{state.count}</h1>
    <button onclick={() => actions.down(1)}>-</button>
    <button onclick={() => actions.up(1)}>+</button>
  </div>
)
app(state, actions, view, socument.body)

const view = (state, actions) => 
  h("div", {}, [
    h("h1", {}, state.count),
    h("button", { onclick: () => actions.down(1) }, "-"),
    h("button", { onclick: () => actions.up(1) }, "+")
  ])
  
import { h, app } from "hyperapp"

const state = {
  count: 0
}

const state = {
  top: {
    count: 0
  },
  bottom: {
    count: 0
  }
}

const actions = {
  setValue: value => ({ value })
}

const actions = {
  down: value => state => ({ count: state.count - value }),
  up: value => state => ({ count: state.count + value })
}

const actions = {
  uplater: value => (state, actions) => {
    setTimeout(actins.up, 1000, value)
  },
  up: value => state => ({ count: state.count + value })
}

const actions = {
  upLater: () => async (state, actions) => {
    await new Promise(done => setTimeout(done, 1000))
    actions.up(10)
  },
  up: value => state => ({ count: state.count + value })
}

count state = {
  counter: {
    count: 0
  }
}

const actions = {
  counter: {
    down: value => state => ({ count: state.count - value }),
    up: value => state => ({ count: state.count + value })
  }
}

const main = app(state, actions, view, document.body)
setInterval(main.up, 250, 1)
setinterval(main.down, 500, 1)

const actions = {
  getState: () => state => state
}

import { h } from "hyperapp"
export const view = (state, actions) =>
  h("div", {}, [
    h("h1", {}, state.count),
    h("button", { onclick: () => actions.down(1) }, "-"),
    h("button", { onclick: () => actions.up(1) }, "+")
  ])

app(state, actions, view, container)

import { h } from "hyperapp"
export const PlayerList = ({ players }) =>
  players
    .slice()
    .sort((player, nextPlayer) => nextPlayer.score - player.score)
    .map(player => (
      <li key={player.username} class={player.isAlive ? "alive" : "dead"}>
        <PlayerProfile {...player} />
      </li>
    ))
    
import { h } from "hyperapp"
export const ImageGallery = ({ images }) =>
  images.map(({ hash, url, description }) => (
    <li key={hash}>
      <img src={url} alt={description} />
    </li>
  ))

import { h } from "hyperapp"
export const Camera = ({ onerror }) => (
  <video
    poster="loading.png"
    oncreate={element => {
      navigator.mediaDevices
        .getUserMedia({ video: true })
        .then(stream => (element.srcObject = stream))
        .catch(onerror)
    }}
    ondestroy={element => element.srcObject.getTracks()[0].stop()}
  />
)
```


```
{
  "plugins": [["@babel/plugin-transform-react-jsx", { "pragma": "h" }]]
}
```


```
npm i hyperapp
```

