```js
// Challenge: Create a UI framework in 1000 chars or less :)~

const _W = window,
      _D = document;

const $ = {},
      G = {},
      L = {};

G.GE = (S, PL=0) => {
  return _D[`querySelector${PL ? 'All' : ''}`](S);
}

G.CE = (T='div', C='', A={}, H=0) => {
  const E = _D.createElement(T);

  E[H ? 'innerHtml' : 'innerText'] = C;

  for (let K in A) {
    E.setAttribute(K, A[K]);
  }

  return E;
};

G.AP = (T, P) => {
    T.appendChild(P);
};

$.R = G.GE('#R');

L.Hello = G.CE('div', 'hellow werld', { 'data-g': 1 });
L.HRU = G.CE('span', 'how are u', { 'data-g': 2 });

G.AP($.R, L.Hello);
G.AP($.R, L.HRU);

// notes:
//   i dunno
```
