# React

## How JSX Compiles

```js
function Comp({name, onChange}) {
    return (
        <div onClick={onChange}>{name}</div>
    )
}
```

```js
function Comp({ name, onChange }) {
    return (React.createElement("div", { onClick: onChange }, name));
}
```

```js
function Comp1({name, onChange}) {
    return (
        <Comp2 onClick={onChange}>{name}</Comp2>
    )
}
```

```js
function Comp({ name, onChange }) {
    return (React.createElement(Comp2, { onClick: onChange }, name));
}
```