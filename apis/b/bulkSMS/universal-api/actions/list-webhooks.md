# BulkSMS: List Webhooks

Retrieves webhooks configured for your BulkSMS account.

```
GET https://connect.mindcloud.co/v1/universal/bulkSMS/latest/actions/list-webhooks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BulkSMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bulkSMS/latest/actions/list-webhooks?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bulkSMS/latest/actions/list-webhooks?${params}`, {
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
      "active": true,
      "contactEmailAddress": "ava@example.com",
      "id": 1,
      "name": "Ava Chen",
      "onWebApp": true,
      "triggerScope": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `contactEmailAddress` | string |  |
| `id` | number |  |
| `name` | string |  |
| `onWebApp` | boolean |  |
| `triggerScope` | string |  |
| `url` | string |  |

## Native endpoint

Through the native BulkSMS API, this operation is `GET /webhooks` (base URL `https://api.bulksms.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-webhooks.md) for the provider-specific parameters and requirements.

