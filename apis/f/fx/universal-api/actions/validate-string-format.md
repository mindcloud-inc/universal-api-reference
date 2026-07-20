# 1001fx: Validate String Format

Validates a string against a supported format.

```
GET https://connect.mindcloud.co/v1/universal/fx/latest/actions/validate-string-format
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 1001fx `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fx/latest/actions/validate-string-format?connectionId=$CONNECTION_ID&format=string&input=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "format": "string",
  "input": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fx/latest/actions/validate-string-format?${params}`, {
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
| `format` | string | yes | String format to validate against. |
| `input` | string | yes | Input value to validate. |
| `options` | object | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "result": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `result` | boolean |  |

## Native endpoint

Through the native 1001fx API, this operation is `POST /data/validatestringformat` (base URL `https://api.1001fx.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/validate-string-format.md) for the provider-specific parameters and requirements.

