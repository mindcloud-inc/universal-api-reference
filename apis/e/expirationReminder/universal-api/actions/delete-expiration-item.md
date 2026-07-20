# Expiration Reminder: Delete Expiration Item

Deletes an expiration item from Expiration Reminder.

```
DELETE https://connect.mindcloud.co/v1/universal/expirationReminder/latest/actions/delete-expiration-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Expiration Reminder `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/expirationReminder/latest/actions/delete-expiration-item?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/expirationReminder/latest/actions/delete-expiration-item?${params}`, {
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

Through the native Expiration Reminder API, this operation is `DELETE /v1/expirationitems/:id` (base URL `https://api.expirationreminder.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-expiration-item.md) for the provider-specific parameters and requirements.

