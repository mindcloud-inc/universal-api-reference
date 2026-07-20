# Brand.dev: Native API Reference

A consolidated summary of Brand.dev's API configuration and 20 documented operations, with links to official documentation.

- **Official docs:** https://docs.context.dev
- **API base URL:** `https://api.brand.dev/v1`

## Authentication

### API Key

Authenticate with a Brand.dev API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.brand.dev/guides/get-started/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Retry behavior

Retry responses with status codes `429`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (20 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Crawl Website Sitemap](actions/crawl-website-sitemap.md) | `GET /web/scrape/sitemap` | [docs](https://docs.context.dev/api-reference/web-scraping/crawl-website-sitemap) |
| [Extract a Single Product from a URL](actions/extract-a-single-product-from-a-url.md) | `POST /brand/ai/product` | [docs](https://docs.context.dev/api-reference/ai-data-extraction/extract-a-single-product-from-a-url) |
| [Extract Design System and Styleguide from Website](actions/extract-design-system-and-styleguide-from-website.md) | `GET /brand/styleguide` | [docs](https://docs.context.dev/api-reference/screenshot-styleguide/extract-design-system-and-styleguide-from-website) |
| [Extract Fonts from Website](actions/extract-fonts-from-website.md) | `GET /brand/fonts` | [docs](https://docs.context.dev/api-reference/screenshot-styleguide/extract-fonts-from-website) |
| [Extract Products from a Brand's Website](actions/extract-products-from-a-brands-website.md) | `POST /brand/ai/products` | [docs](https://docs.context.dev/api-reference/ai-data-extraction/extract-products-from-a-brands-website) |
| [Identify Brand from Transaction Data](actions/identify-brand-from-transaction-data.md) | `GET /brand/transaction_identifier` | [docs](https://docs.context.dev/api-reference/retrieve-brand/identify-brand-from-transaction-data) |
| [Prefetch Brand Data by Email](actions/prefetch-brand-data-by-email.md) | `POST /brand/prefetch-by-email` | [docs](https://docs.context.dev/api-reference/utility/prefetch-brand-data-by-email) |
| [Prefetch Brand Data for a Domain](actions/prefetch-brand-data-for-a-domain.md) | `POST /brand/prefetch` | [docs](https://docs.context.dev/api-reference/utility/prefetch-brand-data-for-a-domain) |
| [Query Website Data Using AI](actions/query-website-data-using-ai.md) | `POST /brand/ai/query` | [docs](https://docs.context.dev/api-reference/ai-data-extraction/query-website-data-using-ai) |
| [Retrieve Brand Data by Company Name](actions/retrieve-brand-data-by-company-name.md) | `GET /brand/retrieve-by-name` | [docs](https://docs.context.dev/api-reference/retrieve-brand/retrieve-brand-data-by-company-name) |
| [Retrieve Brand Data by Domain](actions/retrieve-brand-data-by-domain.md) | `GET /brand/retrieve` | [docs](https://docs.context.dev/api-reference/retrieve-brand/retrieve-brand-data-by-domain) |
| [Retrieve Brand Data by Email Address](actions/retrieve-brand-data-by-email-address.md) | `GET /brand/retrieve-by-email` | [docs](https://docs.context.dev/api-reference/retrieve-brand/retrieve-brand-data-by-email-address) |
| [Retrieve Brand Data by ISIN](actions/retrieve-brand-data-by-isin.md) | `GET /brand/retrieve-by-isin` | [docs](https://docs.context.dev/api-reference/retrieve-brand/retrieve-brand-data-by-isin) |
| [Retrieve Brand Data by Stock Ticker](actions/retrieve-brand-data-by-stock-ticker.md) | `GET /brand/retrieve-by-ticker` | [docs](https://docs.context.dev/api-reference/retrieve-brand/retrieve-brand-data-by-stock-ticker) |
| [Retrieve NAICS Code for Any Brand](actions/retrieve-naics-code-for-any-brand.md) | `GET /brand/naics` | [docs](https://docs.context.dev/api-reference/industry-classification/retrieve-naics-code-for-any-brand) |
| [Retrieve Simplified Brand Data by Domain](actions/retrieve-simplified-brand-data-by-domain.md) | `GET /brand/retrieve-simplified` | [docs](https://docs.context.dev/api-reference/retrieve-brand/retrieve-simplified-brand-data-by-domain) |
| [Scrape Images from a URL](actions/scrape-images-from-a-url.md) | `GET /web/scrape/images` | [docs](https://docs.context.dev/api-reference/web-scraping/scrape-images-from-a-url) |
| [Scrape Raw HTML from a URL](actions/scrape-raw-html-from-a-url.md) | `GET /web/scrape/html` | [docs](https://docs.context.dev/api-reference/web-scraping/scrape-raw-html-from-a-url) |
| [Scrape URL and Convert to Markdown](actions/scrape-url-and-convert-to-markdown.md) | `GET /web/scrape/markdown` | [docs](https://docs.context.dev/api-reference/web-scraping/scrape-url-and-convert-to-markdown) |
| [Take Screenshot of Website](actions/take-screenshot-of-website.md) | `GET /brand/screenshot` | [docs](https://docs.context.dev/api-reference/screenshot-styleguide/take-screenshot-of-website) |
