# <img src="https://images.mindcloud.co/apps/icons/branddev_1774231672935.png" alt="Brand.dev logo" width="28" height="28"> Brand.dev: Universal API

Extract brand, website, and product data from company domains

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/branddev/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 20
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://brand.dev
- **Vendor API docs:** https://docs.context.dev

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Scrape Raw HTML from a URL](actions/scrape-raw-html-from-a-url.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/branddev/latest/actions/scrape-raw-html-from-a-url?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (20)

### Brand

| Action | Method | Description |
| --- | --- | --- |
| [Identify Brand from Transaction Data](actions/identify-brand-from-transaction-data.md) | GET | Identifies a brand from transaction data in Brand.dev. |
| [Retrieve Brand Data by Company Name](actions/retrieve-brand-data-by-company-name.md) | GET | Retrieves brand data from Brand.dev by company name. |
| [Retrieve Brand Data by Domain](actions/retrieve-brand-data-by-domain.md) | GET | Retrieves brand data from Brand.dev by domain. |
| [Retrieve Brand Data by Email Address](actions/retrieve-brand-data-by-email-address.md) | GET | Retrieves brand data from Brand.dev by email address. |
| [Retrieve Brand Data by ISIN](actions/retrieve-brand-data-by-isin.md) | GET | Retrieves brand data from Brand.dev by ISIN. |
| [Retrieve Brand Data by Stock Ticker](actions/retrieve-brand-data-by-stock-ticker.md) | GET | Retrieves brand data from Brand.dev by stock ticker. |
| [Retrieve Simplified Brand Data by Domain](actions/retrieve-simplified-brand-data-by-domain.md) | GET | Retrieves simplified brand data from Brand.dev by domain. |

### Font

| Action | Method | Description |
| --- | --- | --- |
| [Extract Fonts from Website](actions/extract-fonts-from-website.md) | GET | Retrieves website font data from Brand.dev. |

### Html

| Action | Method | Description |
| --- | --- | --- |
| [Scrape Raw HTML from a URL](actions/scrape-raw-html-from-a-url.md) | GET | Retrieves raw HTML from a URL using Brand.dev. |

### Image

| Action | Method | Description |
| --- | --- | --- |
| [Scrape Images from a URL](actions/scrape-images-from-a-url.md) | GET | Retrieves images from a URL using Brand.dev. |

### Industry Classification

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve NAICS Code for Any Brand](actions/retrieve-naics-code-for-any-brand.md) | GET | Retrieves a NAICS code for a brand in Brand.dev. |

### Markdown

| Action | Method | Description |
| --- | --- | --- |
| [Scrape URL and Convert to Markdown](actions/scrape-url-and-convert-to-markdown.md) | GET | Retrieves markdown from a URL using Brand.dev. |

### Prefetch

| Action | Method | Description |
| --- | --- | --- |
| [Prefetch Brand Data by Email](actions/prefetch-brand-data-by-email.md) | POST | Prefetches brand data in Brand.dev by email. |
| [Prefetch Brand Data for a Domain](actions/prefetch-brand-data-for-a-domain.md) | POST | Prefetches brand data in Brand.dev for a domain. |

### Product

| Action | Method | Description |
| --- | --- | --- |
| [Extract a Single Product from a URL](actions/extract-a-single-product-from-a-url.md) | GET | Extracts product data from a URL using Brand.dev. |
| [Extract Products from a Brand's Website](actions/extract-products-from-a-brands-website.md) | GET | Extracts product data from a brand website using Brand.dev. |

### Screenshot

| Action | Method | Description |
| --- | --- | --- |
| [Take Screenshot of Website](actions/take-screenshot-of-website.md) | GET | Retrieves a website screenshot from Brand.dev. |

### Sitemap

| Action | Method | Description |
| --- | --- | --- |
| [Crawl Website Sitemap](actions/crawl-website-sitemap.md) | GET | Retrieves sitemap data from a website using Brand.dev. |

### Styleguide

| Action | Method | Description |
| --- | --- | --- |
| [Extract Design System and Styleguide from Website](actions/extract-design-system-and-styleguide-from-website.md) | GET | Retrieves website styleguide data from Brand.dev. |

### Website Data

| Action | Method | Description |
| --- | --- | --- |
| [Query Website Data Using AI](actions/query-website-data-using-ai.md) | GET | Retrieves website answers using AI in Brand.dev. |

