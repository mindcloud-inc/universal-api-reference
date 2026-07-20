# Hey Reach: List Campaign Leads

Retrieves leads from a Hey Reach campaign.

```
GET https://connect.mindcloud.co/v1/universal/heyReach/latest/actions/list-campaign-leads
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hey Reach `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/heyReach/latest/actions/list-campaign-leads?connectionId=$CONNECTION_ID&limit=25&offset=0&campaignId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "campaignId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/heyReach/latest/actions/list-campaign-leads?${params}`, {
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
| `campaignId` | number | yes |  |
| `offset` | number | no |  |
| `limit` | number | no |  |
| `timeFrom` | date | no |  |
| `timeTo` | date | no |  |
| `timeFilter` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "items": [
        {}
      ],
      "totalCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `items` | array<object> |  |
| `totalCount` | number |  |

## Native endpoint

Through the native Hey Reach API, this operation is `POST /api/public/campaign/GetLeadsFromCampaign` (base URL `https://api.heyreach.io`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-campaign-leads.md) for the provider-specific parameters and requirements.

