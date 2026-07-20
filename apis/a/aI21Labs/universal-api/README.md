# <img src="https://images.mindcloud.co/apps/icons/images-20_1774974194520.jpeg" alt="AI21 Labs logo" width="28" height="28"> AI21 Labs: Universal API

Generate text, plan multi-step AI runs, and manage AI21 file libraries with Jamba and Maestro.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/aI21Labs/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://studio.ai21.com
- **Vendor API docs:** https://docs.ai21.com/reference/introduction

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Library Files](actions/list-library-files.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/aI21Labs/latest/actions/list-library-files?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Library File

| Action | Method | Description |
| --- | --- | --- |
| [List Library Files](actions/list-library-files.md) | GET | Retrieves library files from AI21 Labs. |

### Maestro Run

| Action | Method | Description |
| --- | --- | --- |
| [Analyze Sentiment](actions/analyze-sentiment.md) | POST | Creates a sentiment analysis run in AI21 Labs. |
| [Brainstorm Ideas](actions/brainstorm-ideas.md) | POST | Creates an idea brainstorming run in AI21 Labs. |
| [Classify Text](actions/classify-text.md) | POST | Creates a text classification run in AI21 Labs. |
| [Compare Texts](actions/compare-texts.md) | POST | Creates a text comparison run in AI21 Labs. |
| [Convert To Bullet List](actions/convert-to-bullet-list.md) | POST | Creates a bullet list conversion run in AI21 Labs. |
| [Convert To JSON](actions/convert-to-json.md) | POST | Creates a JSON conversion run in AI21 Labs. |
| [Create Executive Brief](actions/create-executive-brief.md) | POST | Creates an executive brief run in AI21 Labs. |
| [Create Maestro Run](actions/create-maestro-run.md) | POST | Creates a generic Maestro run in AI21 Labs. |
| [Create Outline](actions/create-outline.md) | POST | Creates an outline generation run in AI21 Labs. |
| [Draft Email](actions/draft-email.md) | POST | Creates an email drafting run in AI21 Labs. |
| [Draft Meeting Notes](actions/draft-meeting-notes.md) | POST | Creates a meeting notes run in AI21 Labs. |
| [Evaluate Against Requirements](actions/evaluate-against-requirements.md) | POST | Creates a requirements evaluation run in AI21 Labs. |
| [Explain Technical Concept](actions/explain-technical-concept.md) | POST | Creates a technical explanation run in AI21 Labs. |
| [Extract Keywords](actions/extract-keywords.md) | POST | Creates a keyword extraction run in AI21 Labs. |
| [Extract Structured Data](actions/extract-structured-data.md) | POST | Creates a structured data extraction run in AI21 Labs. |
| [Generate Action Items](actions/generate-action-items.md) | POST | Creates an action item extraction run in AI21 Labs. |
| [Generate Blog Draft](actions/generate-blog-draft.md) | POST | Creates a blog draft run in AI21 Labs. |
| [Generate Checklist](actions/generate-checklist.md) | POST | Creates a checklist generation run in AI21 Labs. |
| [Generate FAQ](actions/generate-faq.md) | POST | Creates an FAQ generation run in AI21 Labs. |
| [Generate Product Description](actions/generate-product-description.md) | POST | Creates a product description run in AI21 Labs. |
| [Generate Social Post](actions/generate-social-post.md) | POST | Creates a social post run in AI21 Labs. |
| [Generate Study Guide](actions/generate-study-guide.md) | POST | Creates a study guide run in AI21 Labs. |
| [Identify Risks](actions/identify-risks.md) | POST | Creates a risk identification run in AI21 Labs. |
| [Retrieve Maestro Run](actions/retrieve-maestro-run.md) | GET | Retrieves a Maestro run by ID from AI21 Labs. |
| [Review Document](actions/review-document.md) | POST | Creates a document review run in AI21 Labs. |
| [Rewrite Text](actions/rewrite-text.md) | POST | Creates a text rewriting run in AI21 Labs. |
| [Simplify Text](actions/simplify-text.md) | POST | Creates a text simplification run in AI21 Labs. |
| [Summarize Text](actions/summarize-text.md) | POST | Creates a text summarization run in AI21 Labs. |
| [Translate Text](actions/translate-text.md) | POST | Creates a text translation run in AI21 Labs. |

