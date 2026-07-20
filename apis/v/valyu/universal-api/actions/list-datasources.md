# Valyu: List Datasources



```
GET https://connect.mindcloud.co/v1/universal/valyu/latest/actions/list-datasources
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Valyu `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/valyu/latest/actions/list-datasources?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/valyu/latest/actions/list-datasources?${params}`, {
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
| `category` | string | no | Filter datasources by category. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "category": "string",
      "coverage": {},
      "description": "string",
      "exampleQueries": [
        "string"
      ],
      "id": "string",
      "languages": [
        "string"
      ],
      "modality": [
        "string"
      ],
      "name": "Ava Chen",
      "pricing": {},
      "responseSchema": {},
      "size": 1,
      "source": "string",
      "topics": [
        "string"
      ],
      "type": "string",
      "updateFrequency": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `category` | string |  |
| `coverage` | object |  |
| `description` | string |  |
| `exampleQueries` | array<string> |  |
| `id` | string |  |
| `languages` | array<string> |  |
| `modality` | array<string> |  |
| `name` | string |  |
| `pricing` | object |  |
| `responseSchema` | object |  |
| `size` | number |  |
| `source` | string |  |
| `topics` | array<string> |  |
| `type` | string |  |
| `updateFrequency` | string |  |

## Native endpoint

Through the native Valyu API, this operation is `GET /datasources` (base URL `https://api.valyu.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-datasources.md) for the provider-specific parameters and requirements.

