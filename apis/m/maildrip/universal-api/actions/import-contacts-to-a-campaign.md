# Maildrip: Import contacts to a campaign



```
POST https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/import-contacts-to-a-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Maildrip `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/import-contacts-to-a-campaign" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "campaignId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/import-contacts-to-a-campaign', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "campaignId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `campaignId` | string | yes | ID of the campaign to import contacts to |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_id": "string",
      "createdAt": "string",
      "failed_uploads": 1,
      "jobType": 1,
      "message": "string",
      "processed": 1,
      "stats": {},
      "status": 1,
      "successful_uploads": 1,
      "total": 1,
      "updatedAt": "string",
      "user": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_id` | string |  |
| `createdAt` | string |  |
| `failed_uploads` | number |  |
| `jobType` | number |  |
| `message` | string |  |
| `processed` | number |  |
| `stats` | object |  |
| `status` | number |  |
| `successful_uploads` | number |  |
| `total` | number |  |
| `updatedAt` | string |  |
| `user` | string |  |

## Native endpoint

Through the native Maildrip API, this operation is `POST /api/v1/{campaignId}/contacts/import` (base URL `https://api.maildrip.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/import-contacts-to-a-campaign.md) for the provider-specific parameters and requirements.

