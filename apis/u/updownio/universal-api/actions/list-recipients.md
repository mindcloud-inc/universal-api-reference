# updown.io: List Recipients

Retrieves all alert recipients from updown.io.

```
GET https://connect.mindcloud.co/v1/universal/updownio/latest/actions/list-recipients
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a updown.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/updownio/latest/actions/list-recipients?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/updownio/latest/actions/list-recipients?${params}`, {
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
      "name": "Ava Chen",
      "type": "string",
      "value": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Recipient identifier. |
| `name` | string | Recipient display name. |
| `type` | string | Recipient channel type. |
| `value` | string | Recipient destination value. |

## Native endpoint

Through the native updown.io API, this operation is `GET /recipients` (base URL `https://updown.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-recipients.md) for the provider-specific parameters and requirements.

