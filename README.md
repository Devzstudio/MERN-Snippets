# MERN-Snippets 🤓

MongoDB, ExpressJS, ReactJS & NodeJS Snippets to Boost the Productivity 🚀
MERN Snippets include Redux, Axios Snippets 😎

## Usage

1. Install the extension
2. You will get suggestion when you type the commands
3. Hit Tab or Enter

## Command

## MongoDB

<table>
<tr>
<th>Shortcut</th>
<th>Description</th>
<th>Output</th>
</tr>
<tbody>

<tr>
<td>req_mongoose</td>
<td>Require Mongoose</td>
<td>
const mongoose = require("mongoose");
</td>
</tr>

<tr>
<td>keys_conf</td>
<td>Mongo key Config</td>
<td>
module.exports = {
  mongoURI:
    ""
};
</td>
</tr>

<tr>
<td>db.keys</td>
<td>Require Mongo Keys</td>
<td>
const db = require("./config/keys").mongoURI;
</td>
</tr>

<tr>
<td>db_connect</td>
<td>Mongoose Connect</td>
<td>
mongoose
  .connect(db)
  .then(() => console.log("💻 Mondodb Connected"))
  .catch(err => console.error(err));
</td>
</tr>

<tr>
<td>db.find</td>
<td>Mongoose find</td>
<td>
Model.find()
    .then(item => res.json(item));</td>
</tr>

<tr>
<td>db.save</td>
<td>Mongoose Save</td>
<td>
const newItem = new Model({
  item: req.body.data
});

newItem.save().then(item => {
res.json(item);
});</td>

</tr>
<tr>
<td>db.delete</td>
<td>Mongoose delete item</td>
<td>
Model.findById(req.params.id)
    .then(item => item.remove().then(() => res.json({ success: true })))
    .catch(err => {
      res.status(400).json({ success: false });
    });
    </td>
</tr>

<tr>
<td>mongoose_schema</td>
<td>Define schema </td>
<td>
const Schema = mongoose.Schema;
</td>
</tr>

<tr>
<td>scheme_export</td>
<td>Export mongo model</td>
<td>
module.exports = Item = mongoose.model("item", itemSchema);
</td>
</tr>

<tr>
<td>scheme</td>
<td>Mongo Schema Model Boilerplate </td>
<td>
const mongoose = require("mongoose");
const Schema = mongoose.Schema;

const itemSchema = new Schema({
name: {
type: String,
required: true
}
});

module.exports = Item = mongoose.model("item", itemSchema);

</td>
</tr>

<tr>
<td>schema_date</td>
<td>Date Type Schema </td>
<td>
date: {
    type: Date,
    default: Date.now
  }
</td>
</tr>

<tr>
<td>schema_string</td>
<td>String Type Schema </td>
<td>
email: {
    type: String,
    required: true
  },
  </td>
 
</tr>

</tbody>
</table>

## ExpressJS

<table>
<tr>
<th>Shortcut</th>
<th>Description</th>
<th>Output</th>
</tr>
<tbody>

<tr>
<td>req_express</td>
<td>Require Express</td>
<td>
const express = require("express");
</td>
</tr>

<tr>
<td>req_bodyparser</td>
<td>Require BodyParser</td>
<td>
const bodyParser = require("body-parser");
</td>
 
</tr>

<tr>
<td>use_bodyparser</td>
<td>Use BodyParser</td>
<td>
app.use(bodyParser.json());
</td>
 
</tr>

<tr>
<td>app.listen</td>
<td>Express app.listen server and PORT</td>
<td>
const port = process.env.PORT || 5000;

app.listen(port, () => `Server running on port ${port} 🔥`);

</td>
</tr>

<tr>
<td>app.get</td>
<td>Express app.get</td>
<td>
app.get("/", (req, res) => {
  
});
</td>
</tr>

<tr>
<td>app.post</td>
<td>Express app.post</td>
<td>
app.post("/", (req, res) => {
  
});
</td>
</tr>

<tr>
<td>exp_router</td>
<td>Express Router Include</td>
<td>
const express = require("express");
const router = express.Router();
</td>
</tr>

<tr>
<td>route_details</td>
<td>Public Route Comment</td>
<td>
/*
    @route GET api/items
    @desc Get all items
    @access public
*/
</td>
</tr>

<tr>
<td>route_details_private</td>
<td>Private Route Comment</td>
<td>
/*
    @route Private api/account
    @desc Get account info
    @access private
*/
</td>
</tr>

<tr>
<td>mod_exp</td>
<td>Module Export</td>
<td>
module.exports = Router;
</td>

</tr>

<tr>
<td>router.get</td>
<td>Get Route</td>
<td>
router.get("/", (req, res) => {
  
});
</td>
</tr>

<tr>
<td>router.post</td>
<td>POST Route</td>
<td>
router.post("/", (req, res) => {
  
});

</td>
</tr>

<tr>
<td>router.delete</td>
<td>Delete Route</td>
<td>
router.delete("/", (req, res) => {
  
});
</td>
</tr>

</tbody>
</table>

## Nodejs

<table>
<tr>
<th>Shortcut</th>
<th>Description</th>
<th>Output</th>
</tr>
<tbody>

<tr>
<td>server</td>
<td>Server.js Boilerplate</td>
<td>
const express = require("express");
const mongoose = require("mongoose");
const bodyParser = require("body-parser");

const app = express();

app.use(bodyParser.json());

const db = require("./config/keys").mongoURI;

mongoose
.connect(db)
.then(() => console.log("💻 Mondodb Connected"))
.catch(err => console.error(err));

app.get("/", (req, res) => {
res.send("Server working 🔥");
});

const port = process.env.PORT || 5000;

app.listen(port, () => `Server running on port port 🔥`);

</td>
</tr>

<tr>
<td>req_path</td>
<td>Require Path</td>
<td>const path = require("path");</td>
</tr>

<tr>
<td>req_http</td>
<td>Require Http</td>
<td>const http = require("http");</td>
</tr>

<tr>
<td>req_fs</td>
<td>Require File Server</td>
<td>const fs = require("fs");</td>
</tr>

<tr>
<td>req_url</td>
<td>Require URL</td>
<td>const url = require("url");</td>
</tr>

</tbody>
</table>

## ReactJS

<table>
<tr>
<th>Shortcut</th>
<th>Description</th>
<th>Output</th>
</tr>
<tbody>

<tr>
<td>imp_react</td>
<td>Import React</td>
<td>import React, { Component } from "react";</td>
</tr>

<tr>
<td>imp_store</td>
<td>Import Store</td>
<td>import store from "./store";</td>
</tr>

<tr>
<td>imp_prop</td>
<td>Import Prop Types</td>
<td>import PropTypes from "prop-types";</td>
</tr>

<tr>
<td>imp_csstrans</td>
<td>Import CSSTransition & Transition Group</td>
<td>
import { CSSTransition, TransitionGroup } from "react-transition-group";
</td>
</tr>

<tr>
<td>imp_provider</td>
<td>Import Provider from React Redux</td>
<td>
import { Provider } from "react-redux";
</td>
</tr>

<tr>
<td>rcc</td>
<td>React Class Component</td>
<td>
import React, { Component } from "react";

class ExampleClass extends Component {
render() {
return (

<div>
Example
</div>
);
}
}

export default ExampleClass;

</td>
</tr>

</tbody>
</table>

## Redux

<table>
<tr>
<th>Shortcut</th>
<th>Description</th>
<th>Output</th>
</tr>
<tbody>

<tr>
<td>imp_connect</td>
<td>Import Connect</td>
<td>
import { connect } from "react-redux";
</td>
</tr>
 
<tr>
<td>reducer</td>
<td>Sample reducer</td>
<td>
export default function(state = initialState, action) {
  switch (action.type) {
    case EXAMPLE:
      return {
        ...state,
        action.payload
      };
     
    default:
      return state;
  }
}
</td>
</tr>

<tr>
<td>store</td>
<td>Store Boilerplate</td>
<td>
import { createStore, applyMiddleware, compose } from "redux";
import thunk from "redux-thunk";
import rootReducer from "./reducers";

const initialState = {};

const middleware = [thunk];

const store = createStore(
rootReducer,
initialState,
compose(
applyMiddleware(...middleware),
window.**REDUX_DEVTOOLS_EXTENSION** && window.**REDUX_DEVTOOLS_EXTENSION**()
)
);

export default store;

</td>
</tr>

<tr>
<td>actions</td>
<td>New redux action</td>
<td>
export const getItems = () => {
  return {
    type: GET_ITEMS
  };
};
</td>
</tr>

<tr>
<td>actions_get</td>
<td>Create action with axios get</td>
<td>
export const getItems = () => dispatch => {
  dispatch(setItemsLoading());
  axios.get("/api/items").then(res =>
    dispatch({
      type: GET_ITEMS,
      payload: res.data
    })
  );
};
</td>

</tr>

<tr>
<td>actions_post</td>
<td>Create action with axios post</td>
<td>
export const getItems = () => dispatch => {
  dispatch(setItemsLoading());
  axios.post("/api/add/items").then(res =>
    dispatch({
      type: ADD_ITEM,
      payload: res.data
    })
  );
};
</td>
</tr>

<tr>
<td>actions_delete</td>
<td>Create action with axios delete</td>
<td>
export const getItems = () => dispatch => {
  dispatch(setItemsLoading());
  axios.delete("/api/items/delete").then(res =>
    dispatch({
      type: DELETE_ITEM,
      payload: res.data
    })
  );
};</td>
</tr>

<tr>
<td>payload</td>
<td>Short for action.payload</td>
<td>
action.payload
</td>
</tr>

<tr>
<td>exp_conn</td>
<td>Export and wrap connect + mapStateToProps</td>
<td>
const mapStateToProps = state => ({
  items: state.item
});

export default connect(
mapStateToProps,
{ getItems }
)(ItemComponent);

</td>
 
</tr>

</tbody>
</table>

## Axios

<table>
<tr>
<th>Shortcut</th>
<th>Description</th>
<th>Output</th>
</tr>
<tbody>

<tr>
<td>imp_axios</td>
<td>Import Axios</td>
<td>
import axios from "axios";
</td>
</tr>

<tr>
<td>axios.get</td>
<td>Axios Get Request</td>
<td>
axios
  .get("/api")
  .then(res => res.data)
  .catch(err => console.error(err));
</td>
</tr>

<tr>
<td>axios.post</td>
<td>Axios Post Request</td>
<td>
axios
  .post("/api")
  .then(res => res.data)
  .catch(err => console.error(err));
</td>
</tr>

<tr>
<td>axios.delete</td>
<td>Axios Delete Request</td>
<td>
axios
  .delete("/api")
  .then(res => res.data)
  .catch(err => console.error(err));
</td>
</tr>

</tbody>
</table>

## MISC

<table>
<tr>
<th>Shortcut</th>
<th>Description</th>
<th>Output</th>
</tr>
<tbody>

<tr>
<td>imp</td>
<td>import {val} from 'val'</td>
<td>import 'Item' from './Item'</td>
</tr>

<tr>
<td>fun</td>
<td>ES6 Arrow function</td>
<td>
clickHandler = (e) => {
    
};
</td>
</tr>

<tr>
<td>cl</td>
<td>Console.log</td>
<td>
    console.log(`data`);
</td>
</tr>

<tr>
<td>cer</td>
<td>Console.error</td>
<td>
    console.error(`data`);
</td>
</tr>

<tr>
<td>exd</td>
<td>export default</td>
<td>
export default Item;
</td>
</tr>

</tbody>
</table>

## Changelog

### 1.2.0

- Added more snippets ⚡️
- Updated Docs 📖

### 1.0.0

Initial release of MERN snippets

**Enjoy!** 🎉🎊
