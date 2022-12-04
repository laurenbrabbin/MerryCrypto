# MerryCrypto 
## Project Description

MerryCrypto is a a cryptocurrency data aggregator with an inbuilt portfolio manager.

## Features
1. Homepage/Cryptocurrency Page - Top 30 cryptocurrencies by market cap. These can be sorted by price, 24hr change, 24hr volume and name.

2. Individual cryptocurrency page. The page includes:
- Coin stats in 3 currencies: USD, GBP and EUR.
- Price chart which displays the price change over a 24hr, 1w and 1m time period.
- Recent news articles related to the coin. The user can click on the button 'read more' to be redirected to the full article.
- Recent tweets regarding the coin.

3. Exchange Page - A page which has data on the top 100 exchanges including trust rank, trust score, 24hr volume and the year the exchange was established. The user can also be redirected to the exchange homepage.

4. News Page - This page includes all the most recent cryptocurrency news. The user can be redirected to the full news article

5. User account - user can register, login and sign out

6. Watchlist - users can favourite cryptocurrencies and view them in their watchlist

7. Portfolio - user can input their cryptocurrency purchases and view their profit and loss.

## Technologies

The application is written in Typescript. The frontend was created using Angular and the backend was created using NestJS. We also used a PostgreSQL database.

# Installation 
## Backend (NestJS) installation

Go to api folder for Nest JS setup. Perform the following instructions in that folder
```bash
$ cd api
```

1. Create Database in PSQL
```bash
$ createdb merrycrypto

# or run command below to specify psql username (if it is different to mac username)
$ createdb -U username merrycrypto
```
2. Install packages
```bash
$ yarn install
```
3. Set up env variables
```bash
$ touch development.env
```
Specify database username and password in development.env file
```env
DB_PASSWORD=""
DB_USERNAME=""
```
4. Specify JWT secret
```bash
$ touch src/config.ts
```

In src/config.ts provide secret for JSON Web Token, it can be any string.
```ts
export const JWT_SECRET = 'super-secret';
```

5. Migrate tables
```bash
$ yarn db:migrate 
```

6. Setting up Crypto Compare API
```
code .env 

CRYPTOCOMPARE_API_KEY=... <- Insert your own api key

```

## Frontend (Angular) installation
```bash
$ cd frontend
$ yarn install
```


## Running the app
To run the app you need to start the server in the api and frontend folder. Once both servers are running visit http://localhost:4200/ to view the homepage.

```bash
$ cd api
$ yarn start
```
```bash
$ cd frontend
$ yarn start
```





[Nest](https://github.com/nestjs/nest) framework TypeScript starter repository.