# Upcoming movies!

### Approach

The chalenge for that project it's build a simple architecture, and connect to a an movie API called TMDB APi. The </br> project have 2 repositories, one for back-end and other for the front-end.The front-end was builded with ReactJs</br>
with desing helper react material ui core. The back-end was used NodeJs with the frame-work AdonisJs, Adonis provide a</br>
a banche of tools, was uses Authentication and migration from AdonisJs. And the database Postgres, the database was used to save the API users, and theirs token's.

### Architecture

`app` - The logic application.</br>
` ---- Controllers/Http` - Here stay the controllers. </br>
` ---- DTO` - Here are the Data Tranfer Objects</br>
` ---- Models` - Here are the models, models can acces de database using Luci(ORM)</br>
` ---- Services` - Here are serves layers, they can access the providers layers, and separete the logic</br>
`config` - The configs for databases, here you can set the startup parâmeters.</br>
`database` - Here are the migrations and the factorys.</br>
`providers/TMDBApi` - The providers has the layer were as made the connection with TMDB API</br>
`start` - Routes, and the server boostrap</br>

### Used Packages

- `AdonisJs` - The nodejs frame-works. </br>
- `Axios` - Library to make HTTP requests. </br>
- `pg` - Used to connect to the Postgres database.</br>
- `url-parse` - Used to parse the url, to brake the one url string in parâmeters.</br>

### Run in localhost

**Requirements: docker, docker-compose, npm, NodeJs, adonisCli**</br>

First install all dependencies. </br>

```bash
npm install
```

Install adonis-cli
```bash
npm i -g @adonisjs/cli
```

Then start the Postegres with docker:

```bash
docker-compose up
```
Then run the migrations service with adonis cli:
```bash
adonis migration:run
```

And finaly start the adonis in dev mode:
```bash
adonis serve --dev
```

Now, the api it's running, and you can use the por `3333` to connect.</br>

connect to [http://localhost:3333](http://localhost:3333)
