# SharpAPI: Native API Reference

A consolidated summary of SharpAPI's API configuration and 34 documented operations, with links to official documentation.

- **Official docs:** https://documenter.getpostman.com/view/31106842/2s9Ye8faUp
- **API base URL:** `https://sharpapi.com/api/v1`

## Authentication

### API Key

Authenticate with your SharpAPI API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://sharpapi.com/en/blog/post/introducing-the-sharpapi-python-client-sdk)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `data.data`. The total page count is read from `data.meta.last_page`. The current page number is read from `data.meta.current_page`.

## Pagination

Use `per_page` in the query string to set the page size. Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (34 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Analyze Product Review Sentiment](actions/analyze-product-review-sentiment.md) | `POST /ecommerce/review_sentiment` | [docs](https://sharpapi.com/en/catalog/ai/e-commerce/product-review-sentiment-checker) |
| [Analyze Travel Review Sentiment](actions/analyze-travel-review-sentiment.md) | `POST /tth/review_sentiment` | [docs](https://sharpapi.com/en/catalog/ai/travel-tourism-hospitality/travel-review-sentiment-checker) |
| [Calculate Flight Duration](actions/calculate-flight-duration.md) | `GET /airports/flight_duration/:departureCodeType/:departureCode/:departureDate/:departureTime/:arrivalCodeType/:arrivalCode/:arrivalDate/:arrivalTime` | [docs](https://sharpapi.com/en/catalog/utility/airports-database-flight-duration-calculator) |
| [Categorize Hospitality Product](actions/categorize-hospitality-product.md) | `POST /tth/hospitality_product_categories` | [docs](https://sharpapi.com/en/catalog/ai/travel-tourism-hospitality/hospitality-product-categorization) |
| [Categorize Product](actions/categorize-product.md) | `POST /ecommerce/product_categories` | [docs](https://sharpapi.com/en/catalog/ai/e-commerce/product-categorization) |
| [Categorize Tours Activities Product](actions/categorize-tours-activities-product.md) | `POST /tth/ta_product_categories` | [docs](https://sharpapi.com/en/catalog/ai/travel-tourism-hospitality/tours-activities-product-categorization) |
| [Detect Addresses](actions/detect-addresses.md) | `POST /content/detect_address` | [docs](https://sharpapi.com/en/catalog/ai/content-marketing-automation/address-detector) |
| [Detect Ai Generated Content](actions/detect-ai-generated-content.md) | `POST /content/detect_ai` | [docs](https://sharpapi.com/en/catalog/ai/content-marketing-automation/ai-content-detector) |
| [Detect Emails](actions/detect-emails.md) | `POST /content/detect_emails` | [docs](https://sharpapi.com/en/catalog/ai/content-marketing-automation/emails-detector) |
| [Detect Phone Numbers](actions/detect-phone-numbers.md) | `POST /content/detect_phones` | [docs](https://sharpapi.com/en/catalog/ai/content-marketing-automation/phone-numbers-detector) |
| [Detect Profanity](actions/detect-profanity.md) | `POST /content/detect_profanities` | [docs](https://sharpapi.com/en/catalog/ai/content-marketing-automation/profanity-detector) |
| [Detect Spam](actions/detect-spam.md) | `POST /content/detect_spam` | [docs](https://sharpapi.com/en/catalog/ai/content-marketing-automation/spam-detector) |
| [Detect Urls](actions/detect-urls.md) | `POST /content/detect_urls` | [docs](https://sharpapi.com/en/catalog/ai/content-marketing-automation/urls-detector) |
| [Generate Custom Thank You Email](actions/generate-custom-thank-you-email.md) | `POST /ecommerce/thank_you_email` | [docs](https://sharpapi.com/en/catalog/ai/e-commerce/custom-thank-you-e-mail-generator) |
| [Generate Job Description](actions/generate-job-description.md) | `POST /hr/job_description` | [docs](https://sharpapi.com/en/catalog/ai/hr-tech/job-description-generator) |
| [Generate Keywords Tags](actions/generate-keywords-tags.md) | `POST /content/keywords` | [docs](https://sharpapi.com/en/catalog/ai/content-marketing-automation/keywords-tags-generator) |
| [Generate Product Description](actions/generate-product-description.md) | `POST /ecommerce/product_description` | [docs](https://sharpapi.com/en/catalog/ai/e-commerce/product-description-generator) |
| [Generate Product Intro](actions/generate-product-intro.md) | `POST /ecommerce/product_intro` | [docs](https://sharpapi.com/en/catalog/ai/e-commerce/product-intro-generator) |
| [Generate Related Job Positions](actions/generate-related-job-positions.md) | `POST /hr/related_job_positions` | [docs](https://sharpapi.com/en/catalog/ai/hr-tech/related-job-positions-generator) |
| [Generate Related Skills](actions/generate-related-skills.md) | `POST /hr/related_skills` | [docs](https://sharpapi.com/en/catalog/ai/hr-tech/related-skills-generator) |
| [Generate Seo Social Media Tags](actions/generate-seo-social-media-tags.md) | `POST /seo/generate_tags` | [docs](https://sharpapi.com/en/catalog/ai/seo/seo-social-media-tags-generator) |
| [Get Airport By Iata Code](actions/get-airport-by-iata-code.md) | `GET /airports/iata/:iata` | [docs](https://sharpapi.com/en/catalog/utility/airports-database-flight-duration-calculator) |
| [Get Airport By Id](actions/get-airport-by-id.md) | `GET /airports/:id` | [docs](https://sharpapi.com/en/catalog/utility/airports-database-flight-duration-calculator) |
| [List Airports](actions/list-airports.md) | `GET /airports` | [docs](https://sharpapi.com/en/catalog/utility/airports-database-flight-duration-calculator) |
| [List Job Positions](actions/list-job-positions.md) | `GET /utilities/job_positions_list` | [docs](https://sharpapi.com/en/catalog/utility/job-positions-api) |
| [Paraphrase Text](actions/paraphrase-text.md) | `POST /content/paraphrase` | [docs](https://sharpapi.com/en/catalog/ai/content-marketing-automation/paraphrase-text) |
| [Parse Invoice](actions/parse-invoice.md) | `POST /finance/parse_invoice` | [docs](https://sharpapi.com/en/catalog/ai/accounting-finance/invoice-parser) |
| [Parse Resume CV](actions/parse-resume-cv.md) | `POST /hr/parse_resume` | [docs](https://sharpapi.com/en/catalog/ai/hr-tech/resume-cv-parsing) |
| [Proofread Text](actions/proofread-text.md) | `POST /content/proofread` | [docs](https://sharpapi.com/en/catalog/ai/content-marketing-automation/proofread-grammar-checker) |
| [Retrieve Skills List](actions/retrieve-skills-list.md) | `GET /utilities/skills_list` | [docs](https://sharpapi.com/en/catalog/utility/skills-database-api) |
| [Score Resume CV Job Match](actions/score-resume-cv-job-match.md) | `POST /hr/resume_job_match_score` | [docs](https://sharpapi.com/en/catalog/ai/hr-tech/resume-cv-job-match-score) |
| [Scrape URL Content](actions/scrape-url-content.md) | `GET /utilities/scrape_url` | [docs](https://sharpapi.com/en/catalog/utility/web-scraping-api) |
| [Summarize Text](actions/summarize-text.md) | `POST /content/summarize` | [docs](https://sharpapi.com/en/catalog/ai/content-marketing-automation/summarize-text) |
| [Translate Text](actions/translate-text.md) | `POST /content/translate` | [docs](https://sharpapi.com/en/catalog/ai/content-marketing-automation/advanced-text-translator) |
