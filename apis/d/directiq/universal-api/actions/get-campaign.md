# DirectIQ: Get campaign

Retrieves a campaign from DirectIQ by ID.

```
GET https://connect.mindcloud.co/v1/universal/directiq/latest/actions/get-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DirectIQ `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/directiq/latest/actions/get-campaign?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/directiq/latest/actions/get-campaign?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
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

Through the native DirectIQ API, this operation is `GET /core/campaign/get/{id}` (base URL `https://rest.directiq.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-campaign.md) for the provider-specific parameters and requirements.

