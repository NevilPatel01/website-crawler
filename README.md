# Website Crawler with Playwright

This project provides a web crawler built using the Playwright library and Crawlee. The crawler fetches web pages, extracts the page title, and stores the results in a dataset. It also follows links on each page and continues crawling. 

## What I Learned

This project provided valuable hands-on experience with building a functional web crawler using modern tools like Playwright and Crawlee. Through this development process, I gained insights into several critical aspects of web crawling and data manipulation:

- **Understanding Website Crawling**:  
  I learned the fundamental concepts of website crawling, including fetching web pages, navigating DOM structures, and systematically following links to traverse a website.

- **Efficient Data Extraction**:  
  Extracting meaningful data like page titles and URLs taught me how to identify and work with specific DOM elements effectively.

- **Data Management and Storage**:  
  By storing extracted data in a structured JSON format, I improved my understanding of data handling, organization, and how to ensure scalability for larger datasets.

- **Using Playwright for Automation**:  
  Playwright’s powerful API introduced me to automating interactions with web pages in a headless environment, which can simulate real-world browsing scenarios seamlessly.

- **Throttle Crawling for Safe Testing**:  
  Implementing limits on the number of crawl requests (e.g., `maxRequestsPerCrawl`) highlighted the importance of respecting server resources and avoiding unintentional overloading.

- **Error Handling and Robust Code**:  
  Setting up error handling during page fetching and link enqueuing helped in creating a more robust and reliable crawler.

- **Extensibility and Customization**:  
  Designing modular handlers (e.g., `requestHandler`) made the crawler adaptable for different crawling use cases, such as extracting other types of information.

This project not only enhanced my technical skills but also provided practical exposure to solving real-world challenges, preparing me to tackle more advanced data automation and processing tasks in the future.


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
    const startUrl = 'https://nevilpatel.com';
    ```
    ### NOTE: Enter your Website URL that you would like to crawl.

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
