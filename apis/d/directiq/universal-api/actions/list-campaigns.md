# DirectIQ: List Campaigns

Retrieves a paginated list of campaigns from DirectIQ.

```
GET https://connect.mindcloud.co/v1/universal/directiq/latest/actions/list-campaigns
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DirectIQ `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/directiq/latest/actions/list-campaigns?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/directiq/latest/actions/list-campaigns?${params}`, {
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
      "campaigns": [
        [
          {}
        ]
      ],
      "nextPageToken": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `campaigns[]` | array<object> |  |
| `campaigns[].campaignTags[]` | array<object> |  |
| `campaigns[].campaignTags[].id` | number |  |
| `campaigns[].campaignTags[].name` | string |  |
| `campaigns[].fromEmail` | string |  |
| `campaigns[].fromName` | string |  |
| `campaigns[].id` | number |  |
| `campaigns[].language` | string |  |
| `campaigns[].lists[]` | array<number> |  |
| `campaigns[].name` | string |  |
| `campaigns[].parentId` | number |  |
| `campaigns[].scheduleTimeUTC` | date |  |
| `campaigns[].segments[]` | array<number> |  |
| `campaigns[].status` | string |  |
| `campaigns[].subject` | string |  |
| `campaigns[].tags[]` | array<number> |  |
| `campaigns[].templateId` | number |  |
| `campaigns[].timeZoneId` | string |  |
| `campaigns[].totalRecipients` | number |  |
| `campaigns[].type` | string |  |
| `nextPageToken` | string |  |

## Native endpoint

Through the native DirectIQ API, this operation is `GET /core/campaign/list` (base URL `https://rest.directiq.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-campaigns.md) for the provider-specific parameters and requirements.

