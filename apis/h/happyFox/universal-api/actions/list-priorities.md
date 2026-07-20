# HappyFox: List Priorities

Retrieves priorities from HappyFox.

```
GET https://connect.mindcloud.co/v1/universal/happyFox/latest/actions/list-priorities
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HappyFox `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/happyFox/latest/actions/list-priorities?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/happyFox/latest/actions/list-priorities?${params}`, {
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
      "default": true,
      "id": 1,
      "name": "Ava Chen",
      "order": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `default` | boolean | Whether this is the default priority. |
| `id` | number | HappyFox priority ID. |
| `name` | string | Priority display name. |
| `order` | number | Sort order for the priority. |

## Native endpoint

Through the native HappyFox API, this operation is `GET /priorities/` (base URL `https://{{credentials.accountDomain}}/api/1.1/json`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-priorities.md) for the provider-specific parameters and requirements.

