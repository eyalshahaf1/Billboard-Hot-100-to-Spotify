# Billboard Hot 100 to Spotify Playlist

This Python application scrapes the Billboard Hot 100 chart for a specific date you choose and automatically creates a private Spotify playlist with those songs.

## Features
- **Scrape Billboard Hot 100**: Allows users to input a specific date (in the `YYYY-MM-DD` format), scrape the Billboard Hot 100 chart from that date, and collect the song titles.
- **Spotify Integration**: Searches Spotify for the scraped songs and adds them to a newly created private playlist in the user’s Spotify account.

## Requirements
Before running the project, ensure you have the following installed:

- Python 3.x
- A Spotify Developer Account (for API credentials)
- `pip` to install Python dependencies

### Required Libraries
- `requests`: For sending HTTP requests to the Billboard website.
- `beautifulsoup4`: For parsing HTML and scraping the Billboard chart.
- `dotenv`: For securely handling sensitive environment variables.
- `spotipy`: A Python library for the Spotify Web API.

You can install all the required libraries by running the following command:

```bash
pip install -r requirements.txt
```

## Setup Instructions

### 1. Clone the Repository

First, clone the repository to your local machine:

```bash
git clone https://github.com/<your_username>/<your_repo_name>.git
cd <your_repo_name>
```

### 2. Install Dependencies

Install the required dependencies by running:

```bash
pip install -r requirements.txt
```

### 3. Set Up Environment Variables

Create a `.env` file in the root of your project and add the following:

```
Client_ID=<Your Spotify Client ID>
Client_Secret=<Your Spotify Client Secret>
SPOTIPY_DISPLAY_NAME=<Your Spotify Username>
URL_REDIRECT=<Your Spotify Redirect URI>
```

> **Note**: You can obtain your `Client_ID`, `Client_Secret`, and `Redirect_URI` by creating an app in the [Spotify Developer Dashboard](https://developer.spotify.com/dashboard/applications).

### 4. Run the Application

Once everything is set up, you can run the application:

```bash
python <your_script_name>.py
```

You will be prompted to enter a date in the format `YYYY-MM-DD`. The app will scrape the Billboard Hot 100 chart for that date, search for the corresponding songs on Spotify, and add them to a new playlist in your Spotify account.

## Example

1. After running the script, you'll see a prompt like this:

   ```
   Which year do you want to travel to? Type the date in this format YYYY-MM-DD:
   ```

2. After entering a date (e.g., `2000-08-25`), the program will scrape the Billboard Hot 100 chart from that day, search for the tracks on Spotify, and automatically create a playlist titled "2000-08-25 Billboard 100" in your Spotify account.

3. If a song from the Billboard chart cannot be found on Spotify, it will be skipped, and a message will be displayed in the terminal.

## Technologies Used

- **Python**: The core programming language for the app.
- **BeautifulSoup**: A Python library for web scraping, used to extract song data from Billboard’s website.
- **Spotipy**: A lightweight Python library for the Spotify Web API, used to interact with Spotify (authenticate, create playlists, add songs).
- **dotenv**: A library to securely manage environment variables for sensitive information (like Spotify credentials).

## Known Issues & Limitations
- Some songs from the Billboard Hot 100 may not exist in the Spotify library and will be skipped.
- Currently, the playlist is always created as private. No option is provided to make it public in this version.
- Spotify API rate limits may affect performance when dealing with a large number of requests.

## Future Improvements
- Add an option for the user to choose between creating a public or private playlist.
- Enhance song matching by incorporating additional search filters (e.g., artist names).

## License

This project is licensed under the MIT License. See the `LICENSE` file for more details.

---

## Contribution

Feel free to fork this repository and contribute! Create a new branch, implement your changes, and submit a pull request for review.

## Contact

If you have any questions or feedback, feel free to open an issue or contact me through [eyal.shahaf1@gmail.com](eyal.shahaf1@gmail.com).

---

Happy coding! 🎵🎶
``` 