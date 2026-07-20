# Minimax: List Files

Retrieves files from Minimax.

```
GET https://connect.mindcloud.co/v1/universal/minimax/latest/actions/list-files
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Minimax `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/minimax/latest/actions/list-files?connectionId=$CONNECTION_ID&purpose=t2a_async_input" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "purpose": "t2a_async_input"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/minimax/latest/actions/list-files?${params}`, {
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
| `purpose` | list | yes | The file purpose to list. One of: `0`, `1`, `2`. Example: `t2a_async_input`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "base_resp": {
        "status_code": 1,
        "status_msg": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `base_resp.status_code` | number |  |
| `base_resp.status_msg` | string |  |

## Native endpoint

Through the native Minimax API, this operation is `GET /v1/files/list` (base URL `https://api.minimax.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-files.md) for the provider-specific parameters and requirements.

