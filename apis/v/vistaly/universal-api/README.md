# <img src="https://images.mindcloud.co/apps/icons/vistaly_1775763654100.png" alt="Vistaly logo" width="28" height="28"> Vistaly: Universal API

Manage product cards, feedback, and metrics in Vistaly

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/vistaly/latest
- **Category:** Productivity / Project Management
- **Actions:** 15
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://vistaly.com
- **Vendor API docs:** https://docs.vistaly.com/api-reference/introduction

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Auth Info](actions/get-auth-info.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vistaly/latest/actions/get-auth-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (15)

### Auth Info

| Action | Method | Description |
| --- | --- | --- |
| [Get Auth Info](actions/get-auth-info.md) | GET | Retrieves auth info from Vistaly. |

### Card

| Action | Method | Description |
| --- | --- | --- |
| [Create Card](actions/create-card.md) | POST | Creates a new card in Vistaly. |
| [Get Card Context](actions/get-card-context.md) | GET | Retrieves card context from Vistaly. |
| [Get Card Details](actions/get-card-details.md) | GET | Retrieves card details from Vistaly. |
| [Search Cards](actions/search-cards.md) | GET | Finds cards in Vistaly by semantic search. |
| [Update Card](actions/update-card.md) | PUT | Updates an existing card in Vistaly. |
| [Update Card Parents](actions/update-card-parents.md) | PUT | Updates a card's parents in Vistaly. |

### Card Metric

| Action | Method | Description |
| --- | --- | --- |
| [Submit Bulk Metrics for Card](actions/submit-bulk-metrics-for-card.md) | POST | Creates bulk metrics for a card in Vistaly. |
| [Submit Metrics for Card](actions/submit-metrics-for-card.md) | POST | Creates metrics for a card in Vistaly. |

### Comment

| Action | Method | Description |
| --- | --- | --- |
| [List Card Comments](actions/list-card-comments.md) | GET | Retrieves comments for a card from Vistaly. |

### Feedback

| Action | Method | Description |
| --- | --- | --- |
| [Delete Feedback](actions/delete-feedback.md) | DELETE | Deletes existing feedback from Vistaly. |
| [Submit User Feedback](actions/submit-user-feedback.md) | POST | Creates user feedback in Vistaly. |

### Health

| Action | Method | Description |
| --- | --- | --- |
| [Health Check](actions/health-check.md) | GET | Retrieves health status from Vistaly. |

### Interview

| Action | Method | Description |
| --- | --- | --- |
| [Get Interview Transcript](actions/get-interview-transcript.md) | GET | Retrieves an interview transcript from Vistaly. |
| [Submit Interview Data](actions/submit-interview-data.md) | POST | Creates interview data in Vistaly. |

