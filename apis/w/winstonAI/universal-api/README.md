# <img src="https://images.mindcloud.co/apps/icons/winston-ai_1774641791427.png" alt="Winston AI logo" width="28" height="28"> Winston AI: Universal API

Detect AI text, plagiarism, facts, images, and text similarity

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/winstonAI/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 5
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://gowinston.ai
- **Vendor API docs:** https://docs.gowinston.ai/api-reference/introduction

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Compare Text](actions/compare-text.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/winstonAI/latest/actions/compare-text?connectionId=$CONNECTION_ID&firstText=Text%20to%20compare%20against%20the%20second%20input&secondText=Second%20text%20to%20compare" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (5)

### Ai Image Detection

| Action | Method | Description |
| --- | --- | --- |
| [Detect AI Image](actions/detect-ai-image.md) | GET |  |

### Ai Text Detection

| Action | Method | Description |
| --- | --- | --- |
| [Detect AI Text](actions/detect-ai-text.md) | GET |  |

### Fact Check

| Action | Method | Description |
| --- | --- | --- |
| [Check Facts](actions/check-facts.md) | GET |  |

### Plagiarism Scan

| Action | Method | Description |
| --- | --- | --- |
| [Check Plagiarism](actions/check-plagiarism.md) | GET |  |

### Text Comparison

| Action | Method | Description |
| --- | --- | --- |
| [Compare Text](actions/compare-text.md) | GET |  |

