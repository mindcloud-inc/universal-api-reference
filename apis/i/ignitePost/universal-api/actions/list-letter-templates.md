# IgnitePost: List Letter Templates

Retrieves available letter templates from IgnitePost.

```
GET https://connect.mindcloud.co/v1/universal/ignitePost/latest/actions/list-letter-templates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a IgnitePost `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ignitePost/latest/actions/list-letter-templates?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ignitePost/latest/actions/list-letter-templates?${params}`, {
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
      "id": 1,
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number | IgnitePOST letter template ID. |
| `name` | string | Display name of the letter template. |

## Native endpoint

Through the native IgnitePost API, this operation is `GET /letter_templates` (base URL `https://dashboard.ignitepost.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-letter-templates.md) for the provider-specific parameters and requirements.

