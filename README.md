Another demonstration of a [custom D3 bundle](/mbostock/bb09af4c39c79cffcde4) using Rollup. This demonstrates importing [d3-transition](https://github.com/d3/d3-transition), which modifies *selection*.prototype to define [*selection*.transition](https://github.com/d3/d3-transition#selection_transition):

```js
import "d3-transition";
```

(There are other features in [d3-transition](https://github.com/d3/d3-transition), but they are not imported here because they are not used.) Note that you *must* also import `selection` from [d3-selection](https://github.com/d3/d3-selection); otherwise, Rollup doesn’t know that it needs to include the imported code from d3-transition. Rollup isn’t perfect at detecting which code needs to be included (and which code shouldn’t be included), so sometimes you need to give it a hand.
