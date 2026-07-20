# TelTel: List SMS Campaign Actions

Retrieves SMS campaign action history from TelTel.

```
GET https://connect.mindcloud.co/v1/universal/telTel/latest/actions/list-sms-campaign-actions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TelTel `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/telTel/latest/actions/list-sms-campaign-actions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/telTel/latest/actions/list-sms-campaign-actions?${params}`, {
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
      "action": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `action` | string |  |
| `createdAt` | date |  |
| `id` | number |  |
| `status` | string |  |

## Native endpoint

Through the native TelTel API, this operation is `GET /sms/campaigns/{id}/actions` (base URL `https://api.teltel.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-sms-campaign-actions.md) for the provider-specific parameters and requirements.

