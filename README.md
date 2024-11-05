# Search Engine

A distributed web crawler and search engine that crawls websites and indexes their content for searching. The system consists of several key components working together to provide efficient web crawling and content indexing capabilities.

## Features

### Web Crawling
- Performs breadth-first crawling of websites starting from a given URL
- Generates unique crawl IDs for tracking different crawl sessions
- Supports setting maximum crawl depth and page limits
- Handles both HTTP and HTTPS URLs

### Distributed Processing
- Uses Kafka for distributed message processing of crawl requests
- Redis for maintaining crawl state and visited URL tracking
- Enables asynchronous crawling with real-time status updates

### Content Indexing
- Indexes crawled page content in Elasticsearch
- Stores page text, URLs, and metadata for searching
- Maintains relationships between base URLs and crawled pages
- Records crawl depth and other metrics

### API Endpoints
- `/api/crawl` - Start a new crawl session
- `/api/crawl/{crawlId}` - Get status of an ongoing crawl
- `/api/sendKafka` - Direct interface to send crawl requests to Kafka
- Swagger UI available at `/swagger-ui.html` for API documentation

### Monitoring
- Real-time crawl status monitoring
- Tracks number of pages crawled
- Records crawl depth and timing information
- Provides crawl completion status and stop reasons

The system is designed to be scalable and can be deployed across multiple nodes for parallel crawling and processing of web content.
