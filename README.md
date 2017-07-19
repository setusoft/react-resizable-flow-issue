Repository which shows a flow issue in [react-resizable](https://github.com/STRML/react-resizable/issues/67).

Execute:
```
yarn flow
```

It prints:
```
λ yarn flow
yarn flow v0.21.3
$ flow check || exit 0
node_modules/react-resizable/build/ResizableBox.js.flow:55
           v---------
 55:       <Resizable
 56:         handleSize={handleSize}
 57:         width={this.state.width}
...:
 67:         >
             ^ props of React element `Resizable`
 56:         handleSize={handleSize}
                         ^^^^^^^^^^ tuple type. This type is incompatible with
 84:     handleSize: [20, 20],
                     ^^^^^^^^ array literal. See: node_modules/react-resizable/build/Resizable.js.flow:84

node_modules/react-resizable/build/ResizableBox.js.flow:55
           v---------
 55:       <Resizable
 56:         handleSize={handleSize}
 57:         width={this.state.width}
...:
 67:         >
             ^ props of React element `Resizable`
 63:         minConstraints={minConstraints}
                             ^^^^^^^^^^^^^^ tuple type. This type is incompatible with
 87:     minConstraints: [20, 20],
                         ^^^^^^^^ array literal. See: node_modules/react-resizable/build/Resizable.js.flow:87

node_modules/react-resizable/build/ResizableBox.js.flow:55
           v---------
 55:       <Resizable
 56:         handleSize={handleSize}
 57:         width={this.state.width}
...:
 67:         >
             ^ props of React element `Resizable`
 64:         maxConstraints={maxConstraints}
                             ^^^^^^^^^^^^^^ tuple type. This type is incompatible with
 88:     maxConstraints: [Infinity, Infinity]
                         ^^^^^^^^^^^^^^^^^^^^ array literal. See: node_modules/react-resizable/build/Resizable.js.flow:88


Found 3 errors
Done in 2.86s.
```
