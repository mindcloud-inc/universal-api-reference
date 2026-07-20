# Prerender.io: List Seo Score Summary

Retrieves an SEO score summary from Prerender.io.

```
GET https://connect.mindcloud.co/v1/universal/prerenderio/latest/actions/get-v3-seo-score-summary
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Prerender.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/prerenderio/latest/actions/get-v3-seo-score-summary?connectionId=$CONNECTION_ID&domainId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "domainId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/prerenderio/latest/actions/get-v3-seo-score-summary?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `domainId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "averageScore": 1,
      "domain": "string",
      "good": 1,
      "needsImprovement": 1,
      "poor": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `averageScore` | number |  |
| `domain` | string |  |
| `good` | number |  |
| `needsImprovement` | number |  |
| `poor` | number |  |

## Native endpoint

Through the native Prerender.io API, this operation is `GET /v3/seo/score/summary` (base URL `https://api.prerender.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-v3-seo-score-summary.md) for the provider-specific parameters and requirements.

