# Maildrip: Update email content for a campaign



```
PUT https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/update-email-content-for-a-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Maildrip `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/update-email-content-for-a-campaign" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "campaignId": "string",
  "emailId": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/update-email-content-for-a-campaign', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "campaignId": "string",
    "emailId": "ava@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `campaignId` | string | yes | ID of the campaign |
| `emailId` | string | yes | ID of the email |

## Response

```json
{
  "success": true,
  "data": [
    {
      "__v": 1,
      "_id": "string",
      "configurations": {},
      "createdAt": "2026-05-07T12:00:00.000Z",
      "emails": [
        {}
      ],
      "interval": 1,
      "name": "Ava Chen",
      "status": true,
      "toggleCount": 1,
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "users": [
        {}
      ],
      "variables": [
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
| `__v` | number | Version of the campaign |
| `_id` | string | ID of the campaign |
| `configurations` | object | Configurations associated with the campaign |
| `createdAt` | date | Timestamp of campaign creation |
| `emails` | array<object> | List of emails associated with the campaign |
| `interval` | number | Interval for the campaign |
| `name` | string | Name of the campaign |
| `status` | boolean | Status of the campaign |
| `toggleCount` | number | Toggle count of the campaign |
| `updatedAt` | date | Timestamp of campaign update |
| `users` | array<object> | List of users associated with the campaign |
| `variables` | array<object> | Variables associated with the campaign |

## Native endpoint

Through the native Maildrip API, this operation is `PATCH /api/v1/campaigns/{campaignId}/{emailId}` (base URL `https://api.maildrip.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-email-content-for-a-campaign.md) for the provider-specific parameters and requirements.

