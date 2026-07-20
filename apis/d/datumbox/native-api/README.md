# Datumbox: Native API Reference

A consolidated summary of Datumbox's API configuration and 13 documented operations, with links to official documentation.

- **Official docs:** https://www.datumbox.com/files/API-Documentation-1.0v.pdf
- **API base URL:** `http://api.datumbox.com/1.0`

## Authentication

### Datumbox API Key

Custom auth for Datumbox requests that send the tenant API key as the form field `api_key`.

### Credentials

- **API Key:** `apiKey` · required · Your Datumbox tenant API key. This credential is stored once and injected into requests as the form field `api_key`.

[Official authentication documentation](https://www.datumbox.com/machine-learning-api/)

## API conventions

Request bodies use URL-encoded form data.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/x-www-form-urlencoded` |

Responses from this API use JSON. Response data is read from `output`.

## Endpoints (13 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Adult Content Detection](actions/adult-content-detection.md) | `POST /AdultContentDetection.json` | [docs](https://www.datumbox.com/files/API-Documentation-1.0v.pdf) |
| [Commercial Detection](actions/commercial-detection.md) | `POST /CommercialDetection.json` | [docs](https://www.datumbox.com/files/API-Documentation-1.0v.pdf) |
| [Document Similarity](actions/document-similarity.md) | `POST /DocumentSimilarity.json` | [docs](https://www.datumbox.com/files/API-Documentation-1.0v.pdf) |
| [Educational Detection](actions/educational-detection.md) | `POST /EducationalDetection.json` | [docs](https://www.datumbox.com/files/API-Documentation-1.0v.pdf) |
| [Keyword Extraction](actions/keyword-extraction.md) | `POST /KeywordExtraction.json` | [docs](https://www.datumbox.com/files/API-Documentation-1.0v.pdf) |
| [Language Detection](actions/language-detection.md) | `POST /LanguageDetection.json` | [docs](https://www.datumbox.com/files/API-Documentation-1.0v.pdf) |
| [Readability Assessment](actions/readability-assessment.md) | `POST /ReadabilityAssessment.json` | [docs](https://www.datumbox.com/files/API-Documentation-1.0v.pdf) |
| [Sentiment Analysis](actions/sentiment-analysis.md) | `POST /SentimentAnalysis.json` | [docs](https://www.datumbox.com/files/API-Documentation-1.0v.pdf) |
| [Spam Detection](actions/spam-detection.md) | `POST /SpamDetection.json` | [docs](https://www.datumbox.com/files/API-Documentation-1.0v.pdf) |
| [Subjectivity Analysis](actions/subjectivity-analysis.md) | `POST /SubjectivityAnalysis.json` | [docs](https://www.datumbox.com/files/API-Documentation-1.0v.pdf) |
| [Text Extraction](actions/text-extraction.md) | `POST /TextExtraction.json` | [docs](https://www.datumbox.com/files/API-Documentation-1.0v.pdf) |
| [Topic Classification](actions/topic-classification.md) | `POST /TopicClassification.json` | [docs](https://www.datumbox.com/files/API-Documentation-1.0v.pdf) |
| [Twitter Sentiment Analysis](actions/twitter-sentiment-analysis.md) | `POST /TwitterSentimentAnalysis.json` | [docs](https://www.datumbox.com/files/API-Documentation-1.0v.pdf) |
