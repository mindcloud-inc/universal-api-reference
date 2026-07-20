# Sender: Get Group



```
GET https://connect.mindcloud.co/v1/universal/sender/latest/actions/get-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sender `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sender/latest/actions/get-group?connectionId=$CONNECTION_ID&id=grp_123" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "grp_123"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sender/latest/actions/get-group?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Group ID. Example: `grp_123`. |

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

Through the native Sender API, this operation is `GET /groups/:id` (base URL `https://api.sender.net/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-group.md) for the provider-specific parameters and requirements.

