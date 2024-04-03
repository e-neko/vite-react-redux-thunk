# vite-react-redux-thunk
Boilerplate for new projects

## steps to recreate

- `yarn create vite <project name> --template react`
- `yarn add react-redux redux redux-thunk`
- `yarn add sass --dev`
- optional: `yarn add @reduxjs/toolkit`


## prepare store
```js
import { configureStore } from '@reduxjs/toolkit';

const storeContainer = {};

storeContainer.store = configureStore({
	//reducer,
	middleware: (getDefaultMiddleware) => getDefaultMiddleware({
		thunk: {
			extraArgument: storeContainer,
		}
	}),
});

export default storeContainer.store as store;
```

## reducers, slices, etc

TBD
