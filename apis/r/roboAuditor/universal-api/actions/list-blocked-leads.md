# RoboAuditor: List Blocked Leads



```
GET https://connect.mindcloud.co/v1/universal/roboAuditor/latest/actions/list-blocked-leads
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RoboAuditor `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/roboAuditor/latest/actions/list-blocked-leads?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/roboAuditor/latest/actions/list-blocked-leads?${params}`, {
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
| `page` | number | no | Page number (starts at 1). |
| `limit` | number | no | Maximum blocked leads per page. |
| `sortBy` | string | no | Field to sort by. |
| `sortDesc` | number | no | Use 1 for descending, 0 for ascending. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {}
      ],
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> | Blocked lead rows. |
| `total` | number | Total number of blocked leads. |

## Native endpoint

Through the native RoboAuditor API, this operation is `GET /blocked_leads` (base URL `https://app.siteauditor.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-blocked-leads.md) for the provider-specific parameters and requirements.

