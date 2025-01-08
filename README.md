# Website Crawler with Playwright

This project provides a web crawler built using the Playwright library and Crawlee. The crawler fetches web pages, extracts the page title, and stores the results in a dataset. It also follows links on each page and continues crawling.

## Features

- Crawls websites using Playwright’s headless browser.
- Extracts and logs page titles.
- Saves crawl data (title and URL) to a dataset.
- Follows links on each page and continues the crawl.
- Configured to limit the number of requests per crawl for safe and efficient testing.

## Prerequisites

- Node.js (>= 16.x)
- Playwright library
- Crawlee library

## Installation

1. Clone this repository or download the code.
2. Install dependencies:

    ```bash
    npm install
    ```

3. Install Playwright and browser dependencies:

    ```bash
    npx playwright install
    ```

## Usage

1. Set the entry URL to start crawling:

    ```js
    const startUrl = 'https://w3schools.com';
    ```

2. Run the crawler:

    ```js
    await crawler.run([startUrl]);
    ```

## Configuration

- `maxRequestsPerCrawl`: Limits the number of requests to 50 for testing purposes.
- `requestHandler`: Handles each crawled page (logs the title, saves to a dataset, and enqueues links).
- `headless`: Uncomment to view the browser window during crawl (default is headless).

## Storage

Crawl data is saved to `./storage/datasets/default` in JSON format.

## License

This project is licensed under the MIT License.
