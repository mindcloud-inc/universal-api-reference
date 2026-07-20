# Atlar: List credit transfer batch results

Retrieves credit transfer batch results from Atlar.

```
GET https://connect.mindcloud.co/v1/universal/atlar/latest/actions/list-credit-transfer-batch-results
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Atlar `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/atlar/latest/actions/list-credit-transfer-batch-results?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/atlar/latest/actions/list-credit-transfer-batch-results?${params}`, {
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
| `id` | string<string> | yes |  |
| `errors` | boolean<string> | no |  |
| `skipped` | boolean<string> | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "items": [
        {}
      ],
      "limit": 1,
      "nextToken": "string",
      "token": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `items` | array<object> |  |
| `limit` | number |  |
| `nextToken` | string |  |
| `token` | string |  |

## Native endpoint

Through the native Atlar API, this operation is `GET /payments/v2beta/credit-transfer-batches/{id}/results` (base URL `https://api.atlar.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-credit-transfer-batch-results.md) for the provider-specific parameters and requirements.

