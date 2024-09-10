# Web Crawler

This is a simple web crawler implemented in Go. It crawls a given website up to a specified number of pages using concurrent goroutines.

## Usage

```
crawler <baseURL> <maxConcurrency> <maxPages>
```

- `baseURL`: The starting URL to begin crawling from.
- `maxConcurrency`: The maximum number of concurrent goroutines to use for crawling.
- `maxPages`: The maximum number of pages to crawl.

## Features

- Concurrent crawling using goroutines
- Configurable maximum concurrency and page limit
- Prints a report of crawled pages and their links

## How it works

1. The program takes command-line arguments for the base URL, maximum concurrency, and maximum pages to crawl.
2. It configures the crawler with the provided parameters.
3. The crawling process starts from the base URL.
4. The program uses goroutines to crawl pages concurrently, respecting the maximum concurrency limit.
5. It continues crawling until it reaches the maximum number of pages or exhausts all links.
6. Finally, it prints a report of the crawled pages and their links.

## Example

```
go run main.go https://example.com 5 100
```

This command will start crawling `https://example.com` using a maximum of 5 concurrent goroutines and will stop after crawling 100 pages or when there are no more links to crawl.

## Error Handling

The program includes basic error handling for:
- Insufficient or excessive command-line arguments
- Invalid input for `maxConcurrency` and `maxPages` (non-integer values)
- Configuration errors

## Dependencies

This project uses only the Go standard library and does not require any external dependencies.

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

