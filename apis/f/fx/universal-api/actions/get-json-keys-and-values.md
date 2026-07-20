# 1001fx: Get JSON Keys and Values

Retrieves JSON object keys and values.

```
GET https://connect.mindcloud.co/v1/universal/fx/latest/actions/get-json-keys-and-values
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 1001fx `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fx/latest/actions/get-json-keys-and-values?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fx/latest/actions/get-json-keys-and-values?${params}`, {
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
| `json` | object | no | JSON object to inspect. |
| `jsonString` | string | no | JSON string to inspect when not passing a JSON object. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "result": {
        "keys": [
          "string"
        ],
        "values": [
          "string"
        ]
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `result.keys` | array<string> |  |
| `result.values` | array |  |

## Native endpoint

Through the native 1001fx API, this operation is `POST /data/getjsonkeysandvalues` (base URL `https://api.1001fx.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-json-keys-and-values.md) for the provider-specific parameters and requirements.

