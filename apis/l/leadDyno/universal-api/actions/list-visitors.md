# LeadDyno: List Visitors

Retrieves visitors from your LeadDyno account.

```
GET https://connect.mindcloud.co/v1/universal/leadDyno/latest/actions/list-visitors
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LeadDyno `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/leadDyno/latest/actions/list-visitors?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/leadDyno/latest/actions/list-visitors?${params}`, {
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
      "affiliate": {},
      "campaign": {},
      "created_at": "string",
      "id": 1,
      "latest_click": "string",
      "lead": {},
      "tracking_code": "string",
      "updated_at": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `affiliate` | object |  |
| `campaign` | object |  |
| `created_at` | string |  |
| `id` | number |  |
| `latest_click` | string |  |
| `lead` | object |  |
| `tracking_code` | string |  |
| `updated_at` | string |  |

## Native endpoint

Through the native LeadDyno API, this operation is `GET /visitors` (base URL `https://api.leaddyno.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-visitors.md) for the provider-specific parameters and requirements.

