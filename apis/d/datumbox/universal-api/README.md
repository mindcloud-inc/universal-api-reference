# <img src="https://images.mindcloud.co/apps/icons/clip-path-group-1_1781651056969.png" alt="Datumbox logo" width="28" height="28"> Datumbox: Universal API

Datumbox is a machine learning text-analysis API for language detection, sentiment analysis, topic classification, keyword extraction, text extraction, and document similarity.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/datumbox/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 13
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.datumbox.com
- **Vendor API docs:** https://www.datumbox.com/files/API-Documentation-1.0v.pdf

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Language Detection](actions/language-detection.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/datumbox/latest/actions/language-detection?connectionId=$CONNECTION_ID&text=Enter%20the%20text%20to%20analyze%20for%20language%20detection." \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (13)

### Categories

| Action | Method | Description |
| --- | --- | --- |
| [Topic Classification](actions/topic-classification.md) | GET | Classifies a document's topic in Datumbox. |

### Documents

| Action | Method | Description |
| --- | --- | --- |
| [Adult Content Detection](actions/adult-content-detection.md) | GET | Detects adult content in a document with Datumbox. |
| [Commercial Detection](actions/commercial-detection.md) | GET | Detects commercial intent in a document with Datumbox. |
| [Document Similarity](actions/document-similarity.md) | GET | Compares two documents for similarity in Datumbox. |
| [Educational Detection](actions/educational-detection.md) | GET | Detects educational intent in a document with Datumbox. |
| [Language Detection](actions/language-detection.md) | GET | Detects a document's language in Datumbox. |
| [Readability Assessment](actions/readability-assessment.md) | GET | Assesses a document's readability in Datumbox. |
| [Sentiment Analysis](actions/sentiment-analysis.md) | GET | Analyzes sentiment for a document in Datumbox. |
| [Spam Detection](actions/spam-detection.md) | GET | Detects spam in a document with Datumbox. |
| [Subjectivity Analysis](actions/subjectivity-analysis.md) | GET | Analyzes a document's subjectivity in Datumbox. |
| [Text Extraction](actions/text-extraction.md) | GET | Extracts clear text from HTML in Datumbox. |
| [Twitter Sentiment Analysis](actions/twitter-sentiment-analysis.md) | GET | Analyzes sentiment for a tweet in Datumbox. |

### Keywords

| Action | Method | Description |
| --- | --- | --- |
| [Keyword Extraction](actions/keyword-extraction.md) | GET | Extracts keywords from a document in Datumbox. |

