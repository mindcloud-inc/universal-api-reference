# Google Mail: List Labels

Retrieves labels from a Gmail mailbox.

```
GET https://connect.mindcloud.co/v1/universal/gmail/latest/actions/list-labels
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Mail `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gmail/latest/actions/list-labels?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gmail/latest/actions/list-labels?${params}`, {
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
      "id": "string",
      "labelListVisibility": "string",
      "messageListVisibility": "string",
      "name": "Ava Chen",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `labelListVisibility` | string |  |
| `messageListVisibility` | string |  |
| `name` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Google Mail API, this operation is `GET /labels` (base URL `https://gmail.googleapis.com/gmail/v1/users/:userId`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-labels.md) for the provider-specific parameters and requirements.

