# Nexiopay: View recipients



```
GET https://connect.mindcloud.co/v1/universal/nexiopay/latest/actions/view-recipients
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nexiopay `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nexiopay/latest/actions/view-recipients?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nexiopay/latest/actions/view-recipients?${params}`, {
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
      "email": "ava@example.com",
      "name": "Ava Chen",
      "recipientId": "string",
      "recipientRef": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `email` | string | Recipient email address. |
| `name` | string | Recipient name. |
| `recipientId` | string | Nexio recipient ID. |
| `recipientRef` | string | External recipient reference. |
| `status` | string | Recipient status. |

## Native endpoint

Through the native Nexiopay API, this operation is `GET /payout/v3/recipient` (base URL `https://api.nexiopaysandbox.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/view-recipients.md) for the provider-specific parameters and requirements.

