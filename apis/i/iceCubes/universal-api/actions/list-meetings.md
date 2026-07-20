# IceCubes: List Meetings



```
GET https://connect.mindcloud.co/v1/universal/iceCubes/latest/actions/list-meetings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a IceCubes `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/iceCubes/latest/actions/list-meetings?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/iceCubes/latest/actions/list-meetings?${params}`, {
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
| `keyword` | string | no | Search by meeting title or keyword. |
| `participant` | string | no | Filter by participant email address. |
| `fromDate` | date | no | Filter meetings from this date forward. |
| `toDate` | date | no | Filter meetings up to this date. |
| `scope` | list | no | Limit results to your personal meetings or the organization scope. One of: `0`, `1`. |
| `tag` | string | no | Filter by tag name. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `hubspotDealId` | string | no | Filter by HubSpot deal ID. |
| `salesforceOpportunityId` | string | no | Filter by Salesforce opportunity ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "meetings": [
        {}
      ],
      "pagination": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `meetings` | array<object> | List of meetings. |
| `pagination` | object | Pagination metadata for the meeting list. |

## Native endpoint

Through the native IceCubes API, this operation is `GET /meetings` (base URL `https://icecubes.app/api/public`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-meetings.md) for the provider-specific parameters and requirements.

