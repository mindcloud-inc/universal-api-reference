# RoboAuditor: Export Leads



```
GET https://connect.mindcloud.co/v1/universal/roboAuditor/latest/actions/export-leads
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RoboAuditor `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/roboAuditor/latest/actions/export-leads?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/roboAuditor/latest/actions/export-leads?${params}`, {
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
      "data": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | string | CSV export content for leads. |

## Native endpoint

Through the native RoboAuditor API, this operation is `GET /leads/export` (base URL `https://app.siteauditor.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/export-leads.md) for the provider-specific parameters and requirements.

