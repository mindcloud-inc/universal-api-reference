# Expiration Reminder: List Document Types

Retrieves document types from Expiration Reminder.

```
GET https://connect.mindcloud.co/v1/universal/expirationReminder/latest/actions/list-document-types
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Expiration Reminder `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/expirationReminder/latest/actions/list-document-types?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/expirationReminder/latest/actions/list-document-types?${params}`, {
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
      "customFields": [
        {}
      ],
      "id": "string",
      "isActive": true,
      "modified": "string",
      "name": "Ava Chen",
      "teamId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `customFields` | array<object> |  |
| `id` | string |  |
| `isActive` | boolean |  |
| `modified` | string |  |
| `name` | string |  |
| `teamId` | string |  |

## Native endpoint

Through the native Expiration Reminder API, this operation is `GET /v1/categories` (base URL `https://api.expirationreminder.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-document-types.md) for the provider-specific parameters and requirements.

