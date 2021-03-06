# MONOPOLY Tracker



## Summary 
Monopoly, the simple finance board game that brings friends and family together to bankrupt each other. Problem is the game last too long. With MONOPOLY Tracker game can simply be paused and resume at ease. MONOPOLY Tracker allow players to
- create multiple games,
- add players
- log player location on the board when the game pause
- log each player’s bought properties
- number of houses and hotel on each property
- and the current cash amount




## Site Demo
![Site](#)

 
## Technologies Used
- HTML - Used to create elements on the DOM
- CSS - Styles html elements on page
- Bootstrap - CSS framework
- Howler - Audio interaction
- Youtube-dl - Download audio from YouTube
- Git - Version control system to track changes to source code
- GitHub - Hosts repository that can be deployed to GitHub Pages
- HeroKu - Plateform to deploy app on cloud
 
## API Call
Querying the information from MySQL database to create new game
```js
    app.post("/api/games",function(req,res){
        db.Game.create({
            name: req.body.name,
            numPlayers: req.body.numPlayers
        }).then(function(result){
            res.json(result);
        })
        .catch(function(error){
            console.log(error);
        });
    });
```

Querying the information from mySQL database to create new player
```js
    app.post("/api/players",function(req,res){
        db.Players.create({
            name: req.body.name,
            token: req.body.token,
            money: req.body.money,
            position: req.body.position,
            GameId: req.body.GameId
        }).then(function(result){
            res.json(result);
        }).catch(function(error){
            console.log(error);
        });
    });
```

Querying the information from MySQL database to create new player properties
```js
    app.post("/api/playerProperties",function(req,res){
        db.playerProperties.create({
            PlayerId: req.body.PlayerId,
            PropertyId: req.body.PropertyId
        }).then(function(result){
            res.json(result);
        }).catch(function(error){
            console.log(error);
        });
    })
```


## API response
- Bootstrap - 
- Howler - 
- Git - Version control system to track changes to source code
- GitHub - Hosts repository that can be deployed to GitHub Pages
- HeroKu - 
 




## Built With

* [HTML](https://developer.mozilla.org/en-US/docs/Web/HTML)
* [CSS](https://developer.mozilla.org/en-US/docs/Web/CSS)
* [Boostrap](https://www.bootstrapcdn.com/)
* [Node.js](https://nodejs.org/en/)
* [Express.js](https://expressjs.com/)
* [Sequelize ORM](https://sequelize.org/)


## Authors


**Andres Felipe Jimenez** 
- [LinkedIn](#)
- [Link to Github](https://github.com/AndresF97)

**Kevin Ko**
- [LinkedIn](#)
- [Link to Github](https://github.com/kokevin678)

**Michael Partin** 
- [LinkedIn](#)
- [Link to Github](https://github.com/rev1311)

**Yali Miranda** 
- [LinkedIn](#)
- [Link to Github](https://github.com/yjmiranda)


MONOPOLY Tracker Project
- [Link to Project]()
