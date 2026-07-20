# <img src="https://images.mindcloud.co/apps/icons/review-stream_1775054452533.png" alt="ReviewStream logo" width="28" height="28"> ReviewStream: Universal API

Collect customer reviews, manage surveys, and run feedback campaigns

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/reviewStream/latest
- **Category:** Productivity / Forms & Surveys
- **Actions:** 2
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://reviewstream.ai/
- **Vendor API docs:** https://support.reviewstream.ai/api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Reviews](actions/list-reviews.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/reviewStream/latest/actions/list-reviews?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (2)

### Review

| Action | Method | Description |
| --- | --- | --- |
| [List Reviews](actions/list-reviews.md) | GET | Retrieves reviews from ReviewStream. |

### Survey

| Action | Method | Description |
| --- | --- | --- |
| [List Surveys](actions/list-surveys.md) | GET | Retrieves surveys from ReviewStream. |

