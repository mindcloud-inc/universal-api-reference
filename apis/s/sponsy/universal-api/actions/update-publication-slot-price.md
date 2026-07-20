# Sponsy: Update Publication Slot Price

Updates a publication slot price in Sponsy.

```
PUT https://connect.mindcloud.co/v1/universal/sponsy/latest/actions/update-publication-slot-price
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sponsy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/sponsy/latest/actions/update-publication-slot-price" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "publicationId": "string",
  "slotId": "string",
  "price": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sponsy/latest/actions/update-publication-slot-price', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "publicationId": "string",
    "slotId": "string",
    "price": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `publicationId` | string | yes | Publication ID from Sponsy. |
| `slotId` | string | yes | Publication slot ID from Sponsy. |
| `price` | number | yes | New slot price. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "jobId": "string",
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `jobId` | string |  |
| `message` | string |  |

## Native endpoint

Through the native Sponsy API, this operation is `PATCH /v1/publications/:publicationId/slots/:slotId` (base URL `https://api.getsponsy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-publication-slot-price.md) for the provider-specific parameters and requirements.

