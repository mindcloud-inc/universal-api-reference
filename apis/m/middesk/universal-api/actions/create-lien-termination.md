# Middesk: Create a termination for a lien

Creates a lien termination in Middesk.

```
POST https://connect.mindcloud.co/v1/universal/middesk/latest/actions/create-lien-termination
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Middesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/middesk/latest/actions/create-lien-termination" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "lienId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/middesk/latest/actions/create-lien-termination', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "lienId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `lienId` | string | yes | ID of the lien to terminate. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "id": "string",
      "lienId": "string",
      "packetNumber": "string",
      "status": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string |  |
| `id` | string |  |
| `lienId` | string |  |
| `packetNumber` | string |  |
| `status` | string |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Middesk API, this operation is `POST /liens/:lien_id/termination` (base URL `https://api.middesk.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-lien-termination.md) for the provider-specific parameters and requirements.

