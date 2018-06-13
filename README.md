# react-ui-tree

React tree component for Porphyry

This project was initially developed for a webpage builder. It maintains an
internal tree structure within the component through
[js-tree](https://github.com/wangzuo/js-tree).

###Modified:

Add remove, add, change in node render.
```js
renderNode(node, id, handleRemoveNode, handleAddNode, forceChange)
```

Use Ctrl+mouse move to move the node.

### Demo

[https://pqx.github.io/react-ui-tree](https://pqx.github.io/react-ui-tree)

### Installation

```sh
npm install react-ui-tree --save
```

### Usage

```javascript
<Tree
  paddingLeft={20}              // left padding for children nodes in pixels
  tree={this.state.tree}        // tree object
  onChange={this.handleChange}  // onChange(tree) tree object changed
  renderNode={this.renderNode}  // renderNode(node) return react element
/>

// a sample tree object
// node.children, node.collapsed, node.leaf properties are hardcoded
{
  "module": "react-ui-tree",
  "children": [{
    "collapsed": true,
    "module": "dist",
    "children": [{
      "module": "node.js"
    }]
  }]
}
```

check [app.js](https://github.com/pqx/react-ui-tree/blob/master/example/app.js)
for a working example

### Development

* npm install
* npm start
* http://localhost:8080/example

### License

MIT
