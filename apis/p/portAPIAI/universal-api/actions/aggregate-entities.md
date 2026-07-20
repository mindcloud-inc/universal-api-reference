# Port API AI: Aggregate Entities

Retrieves aggregated entities from Port.

```
GET https://connect.mindcloud.co/v1/universal/portAPIAI/latest/actions/aggregate-entities
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Port API AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/portAPIAI/latest/actions/aggregate-entities?connectionId=$CONNECTION_ID&func=string&query=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "func": "string",
  "query": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/portAPIAI/latest/actions/aggregate-entities?${params}`, {
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
| `func` | string | yes | Aggregate function |
| `query` | object | yes | Aggregate query |

## Response

```json
{
  "success": true,
  "data": [
    {
      "matchingBlueprints": [
        "string"
      ],
      "ok": true,
      "result": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `matchingBlueprints` | array<string> |  |
| `ok` | boolean |  |
| `result` | number |  |

## Native endpoint

Through the native Port API AI API, this operation is `POST /entities/aggregate` (base URL `https://api.port.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/aggregate-entities.md) for the provider-specific parameters and requirements.

