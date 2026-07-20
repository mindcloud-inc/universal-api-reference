# <img src="https://images.mindcloud.co/apps/icons/sharp-api_1776270170382.png" alt="SharpAPI logo" width="28" height="28"> SharpAPI: Universal API

Generate, analyze, and extract structured content and utility data

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/sharpAPI/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 34
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://sharpapi.com
- **Vendor API docs:** https://documenter.getpostman.com/view/31106842/2s9Ye8faUp

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Retrieve Skills List](actions/retrieve-skills-list.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sharpAPI/latest/actions/retrieve-skills-list?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (34)

### Address Detection Job

| Action | Method | Description |
| --- | --- | --- |
| [Detect Addresses](actions/detect-addresses.md) | POST | Creates an address detection job in SharpAPI. |

### Ai Content Detection Job

| Action | Method | Description |
| --- | --- | --- |
| [Detect Ai Generated Content](actions/detect-ai-generated-content.md) | POST | Creates an AI content detection job in SharpAPI. |

### Airport

| Action | Method | Description |
| --- | --- | --- |
| [Get Airport By Iata Code](actions/get-airport-by-iata-code.md) | GET | Retrieves an airport by IATA code from SharpAPI. |
| [Get Airport By Id](actions/get-airport-by-id.md) | GET | Retrieves an airport from SharpAPI. |
| [List Airports](actions/list-airports.md) | GET | Retrieves airports from SharpAPI. |

### Custom Thank You Email Job

| Action | Method | Description |
| --- | --- | --- |
| [Generate Custom Thank You Email](actions/generate-custom-thank-you-email.md) | POST | Creates a thank you email job in SharpAPI. |

### Email Detection Job

| Action | Method | Description |
| --- | --- | --- |
| [Detect Emails](actions/detect-emails.md) | POST | Creates an email detection job in SharpAPI. |

### Flight Duration

| Action | Method | Description |
| --- | --- | --- |
| [Calculate Flight Duration](actions/calculate-flight-duration.md) | GET | Retrieves flight duration details from SharpAPI. |

### Hospitality Product Categorization Job

| Action | Method | Description |
| --- | --- | --- |
| [Categorize Hospitality Product](actions/categorize-hospitality-product.md) | POST | Creates a hospitality product categorization job in SharpAPI. |

### Invoice

| Action | Method | Description |
| --- | --- | --- |
| [Parse Invoice](actions/parse-invoice.md) | POST | Creates an invoice parsing job in SharpAPI. |

### Job Description

| Action | Method | Description |
| --- | --- | --- |
| [Generate Job Description](actions/generate-job-description.md) | POST | Creates a job description in SharpAPI. |

### Job Position

| Action | Method | Description |
| --- | --- | --- |
| [List Job Positions](actions/list-job-positions.md) | GET | Retrieves job positions from SharpAPI. |

### Keywords Tags

| Action | Method | Description |
| --- | --- | --- |
| [Generate Keywords Tags](actions/generate-keywords-tags.md) | POST | Creates keywords and tags in SharpAPI. |

### Paraphrased Text

| Action | Method | Description |
| --- | --- | --- |
| [Paraphrase Text](actions/paraphrase-text.md) | POST | Creates a text paraphrase job in SharpAPI. |

### Phone Number Detection Job

| Action | Method | Description |
| --- | --- | --- |
| [Detect Phone Numbers](actions/detect-phone-numbers.md) | POST | Creates a phone number detection job in SharpAPI. |

### Product Categorization Job

| Action | Method | Description |
| --- | --- | --- |
| [Categorize Product](actions/categorize-product.md) | POST | Creates a product categorization job in SharpAPI. |

### Product Description Job

| Action | Method | Description |
| --- | --- | --- |
| [Generate Product Description](actions/generate-product-description.md) | POST | Creates a product description job in SharpAPI. |

### Product Intro Job

| Action | Method | Description |
| --- | --- | --- |
| [Generate Product Intro](actions/generate-product-intro.md) | POST | Creates a product intro job in SharpAPI. |

### Product Review Sentiment Job

| Action | Method | Description |
| --- | --- | --- |
| [Analyze Product Review Sentiment](actions/analyze-product-review-sentiment.md) | POST | Creates a product review sentiment job in SharpAPI. |

### Profanity Detection Job

| Action | Method | Description |
| --- | --- | --- |
| [Detect Profanity](actions/detect-profanity.md) | POST | Creates a profanity detection job in SharpAPI. |

### Proofread Text

| Action | Method | Description |
| --- | --- | --- |
| [Proofread Text](actions/proofread-text.md) | POST | Creates a proofreading job in SharpAPI. |

### Related Job Positions

| Action | Method | Description |
| --- | --- | --- |
| [Generate Related Job Positions](actions/generate-related-job-positions.md) | POST | Creates related job positions in SharpAPI. |

### Related Skills

| Action | Method | Description |
| --- | --- | --- |
| [Generate Related Skills](actions/generate-related-skills.md) | POST | Creates a related skills job in SharpAPI. |

### Resume Cv

| Action | Method | Description |
| --- | --- | --- |
| [Parse Resume CV](actions/parse-resume-cv.md) | POST | Creates a resume parsing job in SharpAPI. |

### Resume Cv Job Match Score

| Action | Method | Description |
| --- | --- | --- |
| [Score Resume CV Job Match](actions/score-resume-cv-job-match.md) | POST | Creates a resume job match scoring job in SharpAPI. |

### Scraped Url Content

| Action | Method | Description |
| --- | --- | --- |
| [Scrape URL Content](actions/scrape-url-content.md) | POST | Scrapes content from a URL with SharpAPI. |

### Seo Social Media Tags Job

| Action | Method | Description |
| --- | --- | --- |
| [Generate Seo Social Media Tags](actions/generate-seo-social-media-tags.md) | POST | Creates SEO and social media tags in SharpAPI. |

### Skill

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve Skills List](actions/retrieve-skills-list.md) | GET | Retrieves skills from SharpAPI. |

### Spam Detection Job

| Action | Method | Description |
| --- | --- | --- |
| [Detect Spam](actions/detect-spam.md) | POST | Creates a spam detection job in SharpAPI. |

### Text Summary

| Action | Method | Description |
| --- | --- | --- |
| [Summarize Text](actions/summarize-text.md) | POST | Creates a text summary job in SharpAPI. |

### Tours Activities Product Categorization Job

| Action | Method | Description |
| --- | --- | --- |
| [Categorize Tours Activities Product](actions/categorize-tours-activities-product.md) | POST | Creates a tours activities categorization job in SharpAPI. |

### Translated Text

| Action | Method | Description |
| --- | --- | --- |
| [Translate Text](actions/translate-text.md) | POST | Creates a text translation job in SharpAPI. |

### Travel Review Sentiment Job

| Action | Method | Description |
| --- | --- | --- |
| [Analyze Travel Review Sentiment](actions/analyze-travel-review-sentiment.md) | POST | Creates a travel review sentiment job in SharpAPI. |

### Url Detection Job

| Action | Method | Description |
| --- | --- | --- |
| [Detect Urls](actions/detect-urls.md) | POST | Creates a URL detection job in SharpAPI. |

