# Hey Reach: List Campaigns For Lead

Retrieves campaigns for a lead in Hey Reach.

```
GET https://connect.mindcloud.co/v1/universal/heyReach/latest/actions/list-campaigns-for-lead
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hey Reach `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/heyReach/latest/actions/list-campaigns-for-lead?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/heyReach/latest/actions/list-campaigns-for-lead?${params}`, {
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
| `email` | string | no |  |
| `linkedinId` | string | no |  |
| `profileUrl` | string | no |  |
| `offset` | number | no |  |
| `limit` | number | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "items": [
        {}
      ],
      "leadFullName": "Ava Chen",
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
| `leadFullName` | string |  |
| `totalCount` | number |  |

## Native endpoint

Through the native Hey Reach API, this operation is `POST /api/public/campaign/GetCampaignsForLead` (base URL `https://api.heyreach.io`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-campaigns-for-lead.md) for the provider-specific parameters and requirements.

