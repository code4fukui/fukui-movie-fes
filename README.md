# fukui-movie-fes

> 日本語のREADMEはこちらです: [README.ja.md](README.ja.md)

A simple, static website that displays movie information for the Fukui Movie Festival. The content is dynamically rendered in the browser from a single CSV file.

## Live Demo

**[https://code4fukui.github.io/fukui-movie-fes/](https://code4fukui.github.io/fukui-movie-fes/)**

The main page displays a grid of movie posters on a black background. A separate page provides a full, searchable list of the movie data in a table format.

## Features

-   **Poster Grid View:** Displays movie posters and titles from a CSV file in a clean, responsive grid.
-   **Tabular Data View:** A dedicated page (`list.html`) presents the complete movie dataset in a searchable and sortable table.
-   **Data-Driven:** All content is loaded client-side from `fukui-movie-fes_2024.csv`, making it easy to update.
-   **Zero Build Step:** Built with vanilla JavaScript and web components, requiring no installation or build process.

## How It Works

-   The main page (`index.html`) uses the [CSV.js](https://js.sabae.cc/CSV.js) library to fetch and parse the movie data, then dynamically creates the poster grid.
-   The list page (`list.html`) uses the `<csv-viewer>` web component from [code4fukui/csv-viewer](https://github.com/code4fukui/csv-viewer) to render the CSV data as an interactive table.
-   The entire site is static and hosted on GitHub Pages.

## Data Source

Movie information is sourced from the `fukui-movie-fes_2024.csv` file, which includes the following columns:
-   `id`: Unique identifier
-   `title`: The movie title
-   `image`: The corresponding image file name (e.g., `m1.jpg`)

## Running Locally

1.  Clone this repository.
2.  Serve the project directory with a local web server (e.g., using the VS Code Live Server extension or `python -m http.server`).
3.  Open the provided local URL in your web browser.

*Note: A web server is required to avoid CORS issues when fetching the CSV file.*

## License

MIT License — see [LICENSE](LICENSE).