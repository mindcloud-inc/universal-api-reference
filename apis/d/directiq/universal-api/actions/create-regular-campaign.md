# DirectIQ: Create regular campaign

Creates a regular campaign in DirectIQ.

```
POST https://connect.mindcloud.co/v1/universal/directiq/latest/actions/create-regular-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DirectIQ `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/directiq/latest/actions/create-regular-campaign" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/directiq/latest/actions/create-regular-campaign', {
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
      "campaignTags": [
        [
          {}
        ]
      ],
      "fromEmail": "ava@example.com",
      "fromName": "Ava Chen",
      "id": 1,
      "language": "string",
      "lists": [
        [
          1
        ]
      ],
      "name": "Ava Chen",
      "parentId": 1,
      "scheduleTimeUTC": "2026-05-07T12:00:00.000Z",
      "segments": [
        [
          1
        ]
      ],
      "status": "string",
      "subject": "string",
      "tags": [
        [
          1
        ]
      ],
      "templateId": 1,
      "timeZoneId": "string",
      "totalRecipients": 1,
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `campaignTags[]` | array<object> |  |
| `campaignTags[].id` | number |  |
| `campaignTags[].name` | string |  |
| `fromEmail` | string |  |
| `fromName` | string |  |
| `id` | number |  |
| `language` | string |  |
| `lists[]` | array<number> |  |
| `name` | string |  |
| `parentId` | number |  |
| `scheduleTimeUTC` | date |  |
| `segments[]` | array<number> |  |
| `status` | string |  |
| `subject` | string |  |
| `tags[]` | array<number> |  |
| `templateId` | number |  |
| `timeZoneId` | string |  |
| `totalRecipients` | number |  |
| `type` | string |  |

## Native endpoint

Through the native DirectIQ API, this operation is `POST /core/campaign/create` (base URL `https://rest.directiq.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-regular-campaign.md) for the provider-specific parameters and requirements.

