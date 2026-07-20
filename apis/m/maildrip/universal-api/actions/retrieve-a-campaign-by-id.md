# Maildrip: Retrieve a campaign by ID



```
GET https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/retrieve-a-campaign-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Maildrip `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/retrieve-a-campaign-by-id?connectionId=$CONNECTION_ID&campaignId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "campaignId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/retrieve-a-campaign-by-id?${params}`, {
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
| `campaignId` | string | yes | ID of the campaign to retrieve |

## Response

```json
{
  "success": true,
  "data": [
    {
      "__v": 1,
      "_id": "string",
      "analytics": {},
      "configurations": {},
      "createdAt": "2026-05-07T12:00:00.000Z",
      "emails": [
        {}
      ],
      "interval": 1,
      "name": "Ava Chen",
      "status": true,
      "toggleCount": 1,
      "totalPages": 1,
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "user": "string",
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
| `__v` | number |  |
| `_id` | string |  |
| `analytics` | object |  |
| `configurations` | object |  |
| `createdAt` | date |  |
| `emails` | array<object> |  |
| `interval` | number |  |
| `name` | string |  |
| `status` | boolean |  |
| `toggleCount` | number |  |
| `totalPages` | number |  |
| `updatedAt` | date |  |
| `user` | string |  |
| `users` | array<object> |  |
| `variables` | array<object> |  |

## Native endpoint

Through the native Maildrip API, this operation is `GET /api/v1/campaigns/{campaign_id}` (base URL `https://api.maildrip.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-a-campaign-by-id.md) for the provider-specific parameters and requirements.

