# MoySklad: Create document position

Creates a document position in MoySklad.

```
POST https://connect.mindcloud.co/v1/universal/moySklad/latest/actions/create-document-position
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MoySklad `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/moySklad/latest/actions/create-document-position" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "entityType": "customerorder",
  "id": "28e45ad1-3d81-11f1-0a80-0b450021d671",
  "quantity": "1"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/moySklad/latest/actions/create-document-position', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "entityType": "customerorder",
    "id": "28e45ad1-3d81-11f1-0a80-0b450021d671",
    "quantity": "1"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `entityType` | string | yes | MoySklad document type. Default: `customerorder`. |
| `id` | string | yes | MoySklad document ID. Default: `28e45ad1-3d81-11f1-0a80-0b450021d671`. |
| `quantity` | number | yes | MoySklad quantity argument. Default: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "meta": {},
      "price": 1,
      "quantity": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `meta` | object |  |
| `price` | number |  |
| `quantity` | number |  |

## Native endpoint

Through the native MoySklad API, this operation is `POST entity/:entityType/:id/positions` (base URL `https://api.moysklad.ru/api/remap/1.2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-document-position.md) for the provider-specific parameters and requirements.

