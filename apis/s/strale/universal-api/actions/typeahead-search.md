# Strale: Typeahead Search

Finds capabilities or solutions in Strale by keyword.

```
GET https://connect.mindcloud.co/v1/universal/strale/latest/actions/typeahead-search
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Strale `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/strale/latest/actions/typeahead-search?connectionId=$CONNECTION_ID&q=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "q": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/strale/latest/actions/typeahead-search?${params}`, {
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
| `geo` | string | no | Optional geography filter. |
| `limit` | number | no | Maximum number of results to return. |
| `q` | string | yes | Search query. |
| `type` | string | no | Restrict results to capabilities or solutions. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "category": "string",
      "description": "string",
      "geography": "string",
      "name": "Ava Chen",
      "priceCents": 1,
      "slug": "string",
      "sqs": 1,
      "sqsLabel": "string",
      "stepCount": 1,
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `category` | string | Matched item category. |
| `description` | string | Matched item description. |
| `geography` | string | Geography scope. |
| `name` | string | Matched item name. |
| `priceCents` | number | Price in cents when available. |
| `slug` | string | Matched item slug. |
| `sqs` | number | Strale quality score. |
| `sqsLabel` | string | Human-readable quality label. |
| `stepCount` | number | Solution step count when available. |
| `type` | string | Matched item type. |

## Native endpoint

Through the native Strale API, this operation is `GET /v1/suggest/typeahead` (base URL `https://api.strale.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/typeahead-search.md) for the provider-specific parameters and requirements.

