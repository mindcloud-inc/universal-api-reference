# <img src="https://images.mindcloud.co/apps/icons/api-roulette-fallback-icon_1785429394851.png" alt="Numbers API logo" width="28" height="28"> Numbers API: Universal API

Retrieve number, math, year, date, and random trivia facts from Numbers API. The official public API uses HTTP only; do not send sensitive data.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/numbersAPI/latest
- **Actions:** 5
- **OpenAPI specification:** [openapi.json](openapi.json)

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Date Fact](actions/get-date-fact.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/numbersAPI/latest/actions/get-date-fact?connectionId=$CONNECTION_ID&month=1&day=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (5)

### Fact

| Action | Method | Description |
| --- | --- | --- |
| [Get Date Fact](actions/get-date-fact.md) | GET |  |
| [Get Number Math Fact](actions/get-number-math-fact.md) | GET |  |
| [Get Number Trivia](actions/get-number-trivia.md) | GET |  |
| [Get Random Fact](actions/get-random-fact.md) | GET |  |
| [Get Year Fact](actions/get-year-fact.md) | GET |  |

