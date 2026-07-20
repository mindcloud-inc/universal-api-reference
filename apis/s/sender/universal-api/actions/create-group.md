# Sender: Create Group



```
POST https://connect.mindcloud.co/v1/universal/sender/latest/actions/create-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sender `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sender/latest/actions/create-group" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "title": "VIP Customers"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sender/latest/actions/create-group', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "title": "VIP Customers"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `title` | string | yes | Give a name to your new group. Example: `VIP Customers`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountId": "string",
      "activePhoneCount": 1,
      "activeSubscribers": 1,
      "bouncedCount": 1,
      "created": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "isFavourite": true,
      "isRecalculatingSubscribers": true,
      "modified": "2026-05-07T12:00:00.000Z",
      "phoneCount": 1,
      "recipientCount": 1,
      "title": "string",
      "unsubscribedCount": 1,
      "usedInIntegration": true,
      "userId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | string |  |
| `activePhoneCount` | number |  |
| `activeSubscribers` | number |  |
| `bouncedCount` | number |  |
| `created` | date |  |
| `id` | string |  |
| `isFavourite` | boolean |  |
| `isRecalculatingSubscribers` | boolean |  |
| `modified` | date |  |
| `phoneCount` | number |  |
| `recipientCount` | number |  |
| `title` | string |  |
| `unsubscribedCount` | number |  |
| `usedInIntegration` | boolean |  |
| `userId` | string |  |

## Native endpoint

Through the native Sender API, this operation is `POST /groups` (base URL `https://api.sender.net/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-group.md) for the provider-specific parameters and requirements.

