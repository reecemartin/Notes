const express = require('express');
const app = express();

require()'dotenv/config');

// Import Routes
const postsRoute = require('./routes/posts');

app.use('/posts', postsRoute);

// Routes
app.get('/', (req, res) => {
    res.send('Welcome Home');
});

app.listen(3000);
