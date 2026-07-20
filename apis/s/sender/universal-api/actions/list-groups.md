# Sender: List Groups



```
GET https://connect.mindcloud.co/v1/universal/sender/latest/actions/list-groups
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sender `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sender/latest/actions/list-groups?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sender/latest/actions/list-groups?${params}`, {
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

Through the native Sender API, this operation is `GET /groups` (base URL `https://api.sender.net/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-groups.md) for the provider-specific parameters and requirements.

