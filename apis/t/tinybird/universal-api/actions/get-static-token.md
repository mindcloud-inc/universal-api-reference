# Tinybird: Get Static Token



```
GET https://connect.mindcloud.co/v1/universal/tinybird/latest/actions/get-static-token
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tinybird `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tinybird/latest/actions/get-static-token?connectionId=$CONNECTION_ID&token=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "token": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tinybird/latest/actions/get-static-token?${params}`, {
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
| `token` | string | yes | The required value is the static token itself, not its display name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "description": "string",
      "name": "Ava Chen",
      "scopes": [
        {}
      ],
      "token": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string |  |
| `name` | string |  |
| `scopes` | array<object> |  |
| `token` | string | Static token value; handle as sensitive output. |

## Native endpoint

Through the native Tinybird API, this operation is `GET v0/tokens/:token` (base URL `{{credentials.apiHost}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-static-token.md) for the provider-specific parameters and requirements.

