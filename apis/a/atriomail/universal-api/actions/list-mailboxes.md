# Atriomail: List Mailboxes



```
GET https://connect.mindcloud.co/v1/universal/atriomail/latest/actions/list-mailboxes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Atriomail `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/atriomail/latest/actions/list-mailboxes?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/atriomail/latest/actions/list-mailboxes?${params}`, {
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
      "createdAt": "2026-05-07T12:00:00.000Z",
      "createdBy": 1,
      "domain": "string",
      "domainId": 1,
      "id": 1,
      "mailcowId": 1,
      "name": "Ava Chen",
      "quota": 1,
      "quotaUsed": 1,
      "syncedAt": "2026-05-07T12:00:00.000Z",
      "syncStatus": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `createdAt` | date |  |
| `createdBy` | number |  |
| `domain` | string |  |
| `domainId` | number |  |
| `id` | number |  |
| `mailcowId` | number |  |
| `name` | string |  |
| `quota` | number |  |
| `quotaUsed` | number |  |
| `syncedAt` | date |  |
| `syncStatus` | string |  |
| `updatedAt` | date |  |
| `username` | string |  |

## Native endpoint

Through the native Atriomail API, this operation is `GET /mailboxes` (base URL `https://system.atriomail.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-mailboxes.md) for the provider-specific parameters and requirements.

