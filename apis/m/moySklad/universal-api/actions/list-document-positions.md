# MoySklad: List document positions

Retrieves document positions from MoySklad.

```
GET https://connect.mindcloud.co/v1/universal/moySklad/latest/actions/list-document-positions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MoySklad `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/moySklad/latest/actions/list-document-positions?connectionId=$CONNECTION_ID&entityType=customerorder&id=28e45ad1-3d81-11f1-0a80-0b450021d671" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "entityType": "customerorder",
  "id": "28e45ad1-3d81-11f1-0a80-0b450021d671"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/moySklad/latest/actions/list-document-positions?${params}`, {
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
| `entityType` | string | yes | MoySklad document type. Default: `customerorder`. |
| `id` | string | yes | MoySklad document ID. Default: `28e45ad1-3d81-11f1-0a80-0b450021d671`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "context": {},
      "meta": {},
      "rows": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `context` | object |  |
| `meta` | object |  |
| `rows` | array<object> |  |

## Native endpoint

Through the native MoySklad API, this operation is `GET entity/:entityType/:id/positions` (base URL `https://api.moysklad.ru/api/remap/1.2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-document-positions.md) for the provider-specific parameters and requirements.

