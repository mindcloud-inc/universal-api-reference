# Expiration Reminder: List Files Related to Expiration Items

Retrieves files for expiration items from Expiration Reminder.

```
GET https://connect.mindcloud.co/v1/universal/expirationReminder/latest/actions/list-files-related-to-expiration-items
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Expiration Reminder `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/expirationReminder/latest/actions/list-files-related-to-expiration-items?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/expirationReminder/latest/actions/list-files-related-to-expiration-items?${params}`, {
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
      "content": "string",
      "contentLegth": 1,
      "contentType": "string",
      "created": "string",
      "entityId": "string",
      "entityType": "string",
      "id": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `content` | string |  |
| `contentLegth` | number |  |
| `contentType` | string |  |
| `created` | string |  |
| `entityId` | string |  |
| `entityType` | string |  |
| `id` | string |  |
| `name` | string |  |

## Native endpoint

Through the native Expiration Reminder API, this operation is `GET /v1/attachments/expirationitem` (base URL `https://api.expirationreminder.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-files-related-to-expiration-items.md) for the provider-specific parameters and requirements.

