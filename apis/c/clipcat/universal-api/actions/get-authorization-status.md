# Clipcat: Get Authorization Status

Retrieves authorization status for the current Clipcat workspace.

```
GET https://connect.mindcloud.co/v1/universal/clipcat/latest/actions/get-authorization-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clipcat `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clipcat/latest/actions/get-authorization-status?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clipcat/latest/actions/get-authorization-status?${params}`, {
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
      "message": "string",
      "workspace": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |
| `workspace` | string |  |

## Native endpoint

Through the native Clipcat API, this operation is `GET /v1/auth` (base URL `https://api.clipcat.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-authorization-status.md) for the provider-specific parameters and requirements.

