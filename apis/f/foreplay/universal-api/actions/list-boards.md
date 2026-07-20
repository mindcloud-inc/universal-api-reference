# Foreplay: List Boards

Retrieves your accessible boards from Foreplay.

```
GET https://connect.mindcloud.co/v1/universal/foreplay/latest/actions/list-boards
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Foreplay `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/foreplay/latest/actions/list-boards?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/foreplay/latest/actions/list-boards?${params}`, {
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
      "data": [
        {}
      ],
      "error": {},
      "metadata": {
        "message": "string",
        "processed_at": 1,
        "status_code": 1,
        "success": true
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> | Board results for the authenticated user. |
| `error` | object | Provider error object when the request fails. |
| `metadata` | object | Top-level response metadata. |
| `metadata.message` | string | Provider success message. |
| `metadata.processed_at` | number | Provider processing timestamp in epoch milliseconds. |
| `metadata.status_code` | number | HTTP-style provider status code. |
| `metadata.success` | boolean | Whether the request succeeded. |

## Native endpoint

Through the native Foreplay API, this operation is `GET /api/boards` (base URL `https://public.api.foreplay.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-boards.md) for the provider-specific parameters and requirements.

