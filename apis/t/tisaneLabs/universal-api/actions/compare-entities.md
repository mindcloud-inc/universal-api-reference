# Tisane Labs: Compare Entities

Compares named entities in Tisane Labs.

```
GET https://connect.mindcloud.co/v1/universal/tisaneLabs/latest/actions/compare-entities
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tisane Labs `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tisaneLabs/latest/actions/compare-entities?connectionId=$CONNECTION_ID&language1=en&entity1=Gary%20Youngman%20MD&language2=en&entity2=Gary%20Oldman" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "language1": "en",
  "entity1": "Gary Youngman MD",
  "language2": "en",
  "entity2": "Gary Oldman"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tisaneLabs/latest/actions/compare-entities?${params}`, {
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
| `language1` | string | yes | IETF language tag for the first entity. Example: `en`. |
| `entity1` | string | yes | First compound named entity to compare. Example: `Gary Youngman MD`. |
| `language2` | string | yes | IETF language tag for the second entity. Example: `en`. |
| `entity2` | string | yes | Second compound named entity to compare. Example: `Gary Oldman`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "differences": [
        "string"
      ],
      "result": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `differences` | array<string> | Detected entity differences. |
| `result` | string | Comparison result. |

## Native endpoint

Through the native Tisane Labs API, this operation is `POST /compare/entities` (base URL `https://api.tisane.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/compare-entities.md) for the provider-specific parameters and requirements.

