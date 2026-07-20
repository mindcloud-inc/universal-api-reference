# Expiration Reminder: Renew Expiration Item

Renews an expiration item in Expiration Reminder.

```
PUT https://connect.mindcloud.co/v1/universal/expirationReminder/latest/actions/renew-expiration-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Expiration Reminder `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/expirationReminder/latest/actions/renew-expiration-item" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/expirationReminder/latest/actions/renew-expiration-item', {
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
      "assignedTo": {},
      "attachments": [
        {}
      ],
      "category": {},
      "categoryName": "Ava Chen",
      "contactId": "string",
      "contacts": [
        {}
      ],
      "customFields": [
        {}
      ],
      "details": "string",
      "expirationDate": "string",
      "id": "string",
      "isActive": true,
      "locations": [
        {}
      ],
      "modified": "string",
      "name": "Ava Chen",
      "status": "string",
      "statusId": 1,
      "tags": [
        {}
      ],
      "teamId": "string",
      "timeOfDay": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assignedTo` | object |  |
| `attachments` | array<object> |  |
| `category` | object |  |
| `categoryName` | string |  |
| `contactId` | string |  |
| `contacts` | array<object> |  |
| `customFields` | array<object> |  |
| `details` | string |  |
| `expirationDate` | string |  |
| `id` | string |  |
| `isActive` | boolean |  |
| `locations` | array<object> |  |
| `modified` | string |  |
| `name` | string |  |
| `status` | string |  |
| `statusId` | number |  |
| `tags` | array<object> |  |
| `teamId` | string |  |
| `timeOfDay` | string |  |

## Native endpoint

Through the native Expiration Reminder API, this operation is `PUT /v1/expirationitems/:id/renew` (base URL `https://api.expirationreminder.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/renew-expiration-item.md) for the provider-specific parameters and requirements.

