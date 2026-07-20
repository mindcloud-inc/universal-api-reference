# PreCallAI: List Campaigns

Retrieves campaigns from PreCallAI.

```
GET https://connect.mindcloud.co/v1/universal/preCallAI/latest/actions/list-campaigns
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PreCallAI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/preCallAI/latest/actions/list-campaigns?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/preCallAI/latest/actions/list-campaigns?${params}`, {
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
      "data": {
        "assistant_id": "string",
        "dialer_id": "string",
        "id": "string",
        "is_automation": true,
        "name": "Ava Chen",
        "scheduled_at": "string"
      },
      "message": "string",
      "status": 1,
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> | List of campaigns returned by PreCallAI. |
| `data.assistant_id` | string | Assistant ID used by the campaign. |
| `data.dialer_id` | string | Dialer ID used by the campaign. |
| `data.id` | string | Campaign ID. |
| `data.is_automation` | boolean | Whether automation is enabled for the campaign. |
| `data.name` | string | Campaign name. |
| `data.scheduled_at` | string | Scheduled timestamp for the campaign. |
| `message` | string | Provider status message for listing campaigns. |
| `status` | number | HTTP-style status returned by PreCallAI. |
| `success` | boolean | Whether the campaign list request succeeded. |

## Native endpoint

Through the native PreCallAI API, this operation is `GET /campaign/list` (base URL `https://api.precallai.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-campaigns.md) for the provider-specific parameters and requirements.

