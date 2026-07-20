# JetAPI: Delete Chatter Session

Deletes chatter sessions from JetAPI.

```
DELETE https://connect.mindcloud.co/v1/universal/jetAPI/latest/actions/delete-chatter-session
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a JetAPI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/jetAPI/latest/actions/delete-chatter-session?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/jetAPI/latest/actions/delete-chatter-session?${params}`, {
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
      "customerId": 1,
      "deletedConversationsCount": 1,
      "deletedMessagesCount": 1,
      "meta": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `customerId` | number | Customer identifier whose iframe sessions were targeted. |
| `deletedConversationsCount` | number | Number of deleted conversations. |
| `deletedMessagesCount` | number | Number of deleted messages. |
| `meta` | object | Response metadata. |

## Native endpoint

Through the native JetAPI API, this operation is `DELETE /api/v1/chatter/` (base URL `https://api.jetapi.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-chatter-session.md) for the provider-specific parameters and requirements.

