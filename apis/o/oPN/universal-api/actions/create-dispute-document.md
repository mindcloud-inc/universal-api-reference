# OPN: Create Dispute Document

Creates a new document for a dispute in OPN.

```
POST https://connect.mindcloud.co/v1/universal/oPN/latest/actions/create-dispute-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OPN `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/oPN/latest/actions/create-dispute-document" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/oPN/latest/actions/create-dispute-document', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "string",
      "deleted": true,
      "download_uri": "string",
      "filename": "Ava Chen",
      "id": "string",
      "kind": "string",
      "livemode": true,
      "location": "string",
      "object": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | string |  |
| `deleted` | boolean |  |
| `download_uri` | string |  |
| `filename` | string |  |
| `id` | string |  |
| `kind` | string |  |
| `livemode` | boolean |  |
| `location` | string |  |
| `object` | string |  |

## Native endpoint

Through the native OPN API, this operation is `POST /disputes/:id/documents` (base URL `https://api.omise.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-dispute-document.md) for the provider-specific parameters and requirements.

