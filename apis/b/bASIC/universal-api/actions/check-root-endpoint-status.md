# BASIC: Check Root Endpoint Status

Checks the root endpoint status in BASIC.

```
GET https://connect.mindcloud.co/v1/universal/bASIC/latest/actions/check-root-endpoint-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BASIC `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bASIC/latest/actions/check-root-endpoint-status?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bASIC/latest/actions/check-root-endpoint-status?${params}`, {
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
      "db_conn": true,
      "env": "string",
      "root": true,
      "version": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `db_conn` | boolean |  |
| `env` | string |  |
| `root` | boolean |  |
| `version` | string |  |

## Native endpoint

Through the native BASIC API, this operation is `GET /` (base URL `https://api.basic.tech`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/check-root-endpoint-status.md) for the provider-specific parameters and requirements.

