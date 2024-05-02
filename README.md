# Game Listing Project

This project is a game listing web application built using React, JavaScript, HTML, and Tailwind CSS. It fetches game data from an external API using Axios and displays downloadable game links categorized by different genres or categories.

## Features

- **Dynamic Game Listing**: Display a list of downloadable games based on different categories fetched from an API.
- **Category Filter**: Allow users to filter games by categories such as action, adventure, puzzle, etc.
- **Interactive Interface**: Provide a user-friendly interface to browse and download games.

## Technologies Used

- **React**: Front-end JavaScript library for building user interfaces.
- **JavaScript**: Programming language used for implementing functionality.
- **HTML**: Markup language for structuring the web pages.
- **Tailwind CSS**: Utility-first CSS framework for styling the application.
- **Axios**: Promise-based HTTP client for making API requests.

## Getting Started

To run this project locally, follow these steps:

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/KnightSoul9/Game_Listing_Website.git
   ```

2. **Navigate to Project Directory**:
   ```bash
   cd Game_Listing_Website
   ```

3. **Install Dependencies**:
   ```bash
   npm install
   ```

4. **Start the Development Server**:
   ```bash
   npm start
   ```

5. **Open in Browser**:
   Open your web browser and navigate to `http://localhost:3000` to view the application.

## Usage

- Select a game category from the dropdown menu.
- Browse through the list of games available in the selected category.
- Click on the download link to download the desired game.

## API Integration

This project uses Axios to fetch game data from an external API. You will need to replace `API_ENDPOINT` in the code with the actual API endpoint URL. Here's how to integrate the API:

1. **Get API Endpoint**: Sign up on a game API provider (e.g., [GameAPI.com](https://gameapi.com/)).
2. **Replace API Endpoint**: In the codebase, replace `API_ENDPOINT` with the actual API endpoint URL.

```javascript
import axios from "axios";
const key="18d8dc115d954615a6fe8522598e8a97"
const axioCreate= axios.create({
    baseURL: "https://api.rawg.io/api",
    // params: {
    //   key: "18d8dc115d954615a6fe8522598e8a97",
    // },
  });
  
const getPopularGame=axioCreate.get('/games?key='+key)
const getMovieDetails=(id)=>axioCreate.get('/games/'+id+'/movies')
const getGameListByGenreId=(id)=>axioCreate.get('/games?key='+key+'&genres='+id)
```

## Contributing

Contributions are welcome! If you have any suggestions, improvements, or new features to propose, please feel free to open an issue or submit a pull request.

## License

This project is licensed under the [MIT License](LICENSE).

---

**Author**: Satyam 
**Contact**: satysatyam14@gmail.com
**Project Link**: [GitHub](https://github.com/KnightSoul9/Game_Listing_Website)

Enjoy exploring and downloading games with ease! 🎮🕹
