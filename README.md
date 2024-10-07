# Twitch Frontend

Url：https://3zkx3mvm3q.us-west-2.awsapprunner.com/

Backend：

This project is a frontend application for browsing Twitch streams, videos, and clips. It is built using React and Ant Design.

## Table of Contents

- [Features](#features)
- [Technical Frameworks](#technical-frameworks)
- [Architecture](#architecture)
- [Installation](#installation)
- [Usage](#usage)
- [Configuration](#configuration)
- [API Endpoints](#api-endpoints)

## Features

- **Streams**: View a list of live streams. Each stream includes a link to the broadcaster's Twitch page.
- **Videos**: Browse through a collection of videos. Each video includes a link to its Twitch page.
- **Clips**: Explore various clips. Each clip includes a link to its Twitch page.
- **Favorites**: Add or remove streams, videos, and clips from your favorites list.
- **Recommendations**: Get personalized recommendations based on your preferences.
- **Search**: Search for games by name or ID.

## Technical Frameworks

- **React**: A JavaScript library for building user interfaces.
- **Ant Design**: A React UI library that provides a set of high-quality components.
- **Fetch API**: Used for making HTTP requests to the backend server.

## Architecture

The application follows a component-based architecture using React. The main components are:

- **Home**: The main component that renders the tabs for streams, videos, and clips.
- **CardGrid**: A component that renders a grid of cards for each category.
- **CardTitle**: A component that renders the title of each card, including favorite functionality and links.

## Installation

1. Clone the repository:
    ```sh
    git clone 
    ```
2. Navigate to the project directory:
    ```sh
    cd twitchfe
    ```
3. Install the dependencies:
    ```sh
    npm install
    ```

## Usage

1. Start the development server:
    ```sh
    npm start
    ```
2. Open your browser and navigate to `http://localhost:3000`.

## Configuration

- **Proxy**: The project uses a proxy setting in `package.json` to forward API requests to the backend server running on `http://localhost:8080`.

## API Endpoints

- **Top Games**: Fetch the top games from the backend.
    ```javascript
    import { getTopGames } from './utils';
    getTopGames().then(games => console.log(games));
    ```
- **Game Details**: Fetch details of a specific game by name.
    ```javascript
    import { searchGameByName } from './utils';
    searchGameByName('game_name').then(game => console.log(game));
    ```
- **Favorite Items**: Add, delete, and fetch favorite items.
    ```javascript
    import { addFavoriteItem, deleteFavoriteItem, getFavoriteItem } from './utils';
    addFavoriteItem(item).then(() => console.log('Added to favorites'));
    deleteFavoriteItem(item).then(() => console.log('Removed from favorites'));
    getFavoriteItem().then(favs => console.log(favs));
    ```
- **Recommendations**: Fetch recommended items based on user preferences.
    ```javascript
    import { getRecommendations } from './utils';
    getRecommendations().then(recs => console.log(recs));
    ```
- **Search Game by ID**: Search for a game by its ID.
    ```javascript
    import { searchGameById } from './utils';
    searchGameById('game_id').then(game => console.log(game));
    ```
- **Search Game by Name**: Search for a game by its name.
    ```javascript
    import { searchGameByName } from './utils';
    searchGameByName('game_name').then(game => console.log(game));
    ```
