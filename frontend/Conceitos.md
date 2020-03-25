# Conceitos que foram passados

## Props - propriedades

```js
// src/index.js

import React from 'react';
import ReactDOM from 'react-dom';
import App from './App';

ReactDOM.render(
  <React.StrictMode>
    <App />
  </React.StrictMode>,
  document.getElementById('root')
);

```

```js
// src/App

import React from 'react';

import Header from './Header';

function App() {
  return (
    <Header title="Semana OmniStack - por props">
      Semana OmniStack - por children
    </Header>
  );
}

export default App;
```

```js
// src/Header  component

import React from 'react';

export default function Header(/* props */{ title, children }) {
  return (
    <header>
      <h1>
        {/* props. */title}
        <br/>
        {/* props. */children}
      </h1>
    </header>
  )
}
```

## State - Estado do componente

```js
// src/Header  component

import React from 'react';

export default function Header({ children }) {
  return (
    <header>
      <h1>
        {children}
      </h1>
    </header>
  )
}
```

```js
// src/App.js

import React, { useState } from 'react';

import Header from './Header';

function App() {
  const [counter, setCounter] = useState(0);

  function increment() {
    setCounter(counter + 1);

    console.log(counter);
  }

  return (
    <div>
      <Header>Contador: {counter}</Header>
      <button onClick={increment}>Incrementar</button>
    </div>
  );
}

export default App;
```
