import express  from "express";
import bodyParser from "body-parser";
import mongoose  from "mongoose";
import cors from "cors";

import postRoutes from './routes/posts.js';

const app =express();

app.use('/', postRoutes);


app.use(bodyParser.json({limit: '30mb' , extended:true}));
app.use(bodyParser.urlencoded({limit: '30mb' , extended:true}));
app.use(cors());



const CONNECTION_URL = `mongodb+srv://project:project123@cluster0.75zh6.mongodb.net/myFirstDatabase?retryWrites=true&w=majority`; 
const PORT = process.env.PORT || 5000;
mongoose.connect(CONNECTION_URL, {useNewUrlParser : true, useUnifiedTopology:true})
.then(()=> {app.listen(PORT, ()=>console.info(`This Port Running On: ${PORT} `))})
.catch((error)=> {error.message});
//mongoose.set('useFindAnd Modify', false);
