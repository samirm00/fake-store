# fake-store

> React app fake store allows the user to see different items in the shop nd select a specific item to get more detail information.

## Table of contents

- [General info](#general-info)
- [Screenshots](#screenshots)
- [Technologies](#technologies)
- [Setup](#setup)
- [Features](#features)
- [Status](#status)
- [Inspiration](#inspiration)
- [Contact](#contact)

## General info

> A React app , the objective using Redux to mange the global state(store) and integrated with React

## Screenshots

![Example screenshot](./Screenshot.png)

## Technologies

- Node 14.16.0
- React 17.0.2
- Redux 4.0.5
- React-redux 7.2.3

## Setup

- `npm install `
- `npm start`

## Code Examples

```js
/**
 * Reducers : are functions
 * they take two argument :
 * 1- the initial state
 * 2- the action function return {object}
 * Reducers return the new global state(store) after the dispatch
 */

import { actionTypes } from "../contants/action-types";

const initialState = {
  products: [],
};

export const productReducer = (state = initialState, { type, payload }) => {
  switch (type) {
    case actionTypes.SET_PRODUCTS:
      return { ...state, products: payload };
    default:
      return state;
  }
};

export const selectedProductReducer = (state = {}, { type, payload }) => {
  switch (type) {
    case actionTypes.SELECTED_PRODUCT:
      return { ...state, ...payload };
    case actionTypes.REMOVE_SELECTED_PRODUCT:
      return {};
    default:
      return state;
  }
};
```

## Features

List of features ready and Todos for future development

-
-
-

To-do list:

-
-

## Status

Project is: _in progress_

## Inspiration

Learn React Redux by Malvia

## Contact

By [samirm00]
