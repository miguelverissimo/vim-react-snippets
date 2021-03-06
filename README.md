# Vim React Snippets (Fork of epilande/vim-react-snippets)

All credit goes to Epilande. Original @ [vim-react-snippets](https://github.com/epilande/vim-react-snippets).

--
Requires [UltiSnips](https://github.com/SirVer/ultisnips).

![vim-react-snippets](http://i.imgur.com/ImgaW2k.gif)

## Installation

Using [vim-plug](https://github.com/junegunn/vim-plug):

```vim
" ES2015 code snippets (Optional)
Plug 'epilande/vim-es2015-snippets'

" React code snippets
Plug 'miguelverissimo/vim-react-snippets'

" Ultisnips
Plug 'SirVer/ultisnips'

""" Utilsnips trigger configuration (Optional)
let g:UltiSnipsExpandTrigger="<C-l>"
let g:UltiSnipsJumpForwardTrigger="<M-]>"
let g:UltiSnipsJumpBackwardTrigger="<M-[>"
```

## Usage
In a JavaScript or JSX file, type a trigger name while in Insert mode, then press Ultisnips trigger key. In my case I have it mapped to `<C-l>`.

For example, let's say we have `ListItem.js`

In Insert mode

```javascript
rfce<C-l>
```

Will expand to

```javascript
import React from 'react';
import PropTypes from 'prop-types';
import styles from './ListItem.css';

function ListItem({ ...props }) {
  return (
    <div className={styles.base}>

    </div>
  );
}

ListItem.defaultProps = {
};

ListItem.propTypes = {
};

export default ListItem;
```

Check out [`UltiSnips/javascript.snippets`](UltiSnips/javascript.snippets) to see all snippets.


## Snippets

#### Skeleton

| Trigger  | Content |
| -------: | ------- |
| `rrcc→`  | React Redux Class Component |
| `rcc→`   | React Class Component |
| `rcce→`  | React Class Component (extended) |
| `rfc→`   | React Functional Component |
| `rnfc→`  | React (next) Functional Component |
| `rfce→`  | React Functional Component (extended) |
| `rsc→`   | React Styled Component |
| `rsci→`  | React Styled Component Interpolation |


#### Lifecycle

| Trigger  | Content |
| -------: | ------- |
| `cwm→`   | `componentWillMount() {...}` |
| `cdm→`   | `componentDidMount() {...}` |
| `cwrp→`  | `componentWillReceiveProps(nextProps) {...}` |
| `scup→`  | `shouldComponentUpdate(nextProps, nextState) {...}` |
| `cwup→`  | `componentWillUpdate(nextProps, nextState) {...}` |
| `cdup→`  | `componentDidUpdate(prevProps, prevState) {...}` |
| `cwu→`   | `componentWillUnmount() {...}` |
| `ren→`   | `render() {...}` |


#### PropTypes

| Trigger    | Content |
| -------:   | ------- |
| `pt→`      | `propTypes {...}` |
| `pt.a→`    | `PropTypes.array` |
| `pt.b→`    | `PropTypes.bool` |
| `pt.f→`    | `PropTypes.func` |
| `pt.n→`    | `PropTypes.number` |
| `pt.o→`    | `PropTypes.object` |
| `pt.s→`    | `PropTypes.string` |
| `pt.no→`   | `PropTypes.node` |
| `pt.e→`    | `PropTypes.element` |
| `pt.io→`   | `PropTypes.instanceOf` |
| `pt.one→`  | `PropTypes.oneOf` |
| `pt.onet→` | `PropTypes.oneOfType (Union)` |
| `pt.ao→`   | `PropTypes.arrayOf (Instances)` |
| `pt.oo→`   | `PropTypes.objectOf` |
| `pt.sh→`   | `PropTypes.shape` |
| `ir→`      | `isRequired` |

#### Others

| Trigger  | Content |
| -------: | ------- |
| `props→` | `this.props` |
| `state→` | `this.state` |
| `set→`   | `this.setState(...)` |
| `dp→`    | `defaultProps {...}` |
| `cn→`    | `className` |
| `ref→`   | `ref` |
| `pp→`    | `${props => props}` |

#### Hooks

| Trigger  | Content |
| -------: | ------- |
| `us.s→`  | `const [state, setState] = useState('');` |
| `us.e→`  | `useEffect(() => { });`                   |
| `us.er→` | `useEffect(() => { return () => {}; });`  |
| `us.c→`  | `const context = useContext(ctx);`        |
| `us.r→`  | `const [store, dispatch] = useReducer(storeReducer, initialState);` |
| `us.cb→` | `useCallback(() => {  }, []);` |
| `us.m→`  | `const memo = useMemo(() => {  }, []);` |
