const express = require('express');
const app = express();
const port = 8080;

app.get('/:route/:subroute?', (req, res) => {
    if(req.params.subroute){
        res.send(`GET request to route: ${req.params.route} and subroute: ${req.params.subroute}`);
    } else {
        res.send(`GET request to route: ${req.params.route}`);
    }
});

app.post('/:route/:subroute?', (req, res) => {
    if(req.params.subroute){
        res.send(`POST request to route: ${req.params.route} and subroute: ${req.params.subroute}`);
    } else {
        res.send(`POST request to route: ${req.params.route}`);
    }
});

app.listen(port, () => {
    console.log(`Servidor rodando na porta ${port}`);
});# cd-5
