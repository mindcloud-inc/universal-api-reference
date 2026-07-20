# Browser Use: List Sessions

Retrieves sessions from Browser Use.

```
GET https://connect.mindcloud.co/v1/universal/browserUse/latest/actions/list-sessions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Browser Use `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/browserUse/latest/actions/list-sessions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/browserUse/latest/actions/list-sessions?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `page` | number | no | Page number, 1-indexed. Default: `1`. |
| `pageSize` | number | no | Number of sessions per page, maximum 100. Default: `20`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "page": 1,
      "pageSize": 1,
      "sessions": [
        {}
      ],
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `page` | number |  |
| `pageSize` | number |  |
| `sessions` | array<object> |  |
| `total` | number |  |

## Native endpoint

Through the native Browser Use API, this operation is `GET /sessions` (base URL `https://api.browser-use.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-sessions.md) for the provider-specific parameters and requirements.

