# Expiration Reminder: Update Location

Updates an existing location in Expiration Reminder.

```
PUT https://connect.mindcloud.co/v1/universal/expirationReminder/latest/actions/update-location
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Expiration Reminder `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/expirationReminder/latest/actions/update-location" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/expirationReminder/latest/actions/update-location', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
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
      "modified": "string",
      "name": "Ava Chen",
      "parentLocationId": "string",
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
| `modified` | string |  |
| `name` | string |  |
| `parentLocationId` | string |  |
| `teamId` | string |  |

## Native endpoint

Through the native Expiration Reminder API, this operation is `PUT /v1/locations/:id` (base URL `https://api.expirationreminder.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-location.md) for the provider-specific parameters and requirements.

