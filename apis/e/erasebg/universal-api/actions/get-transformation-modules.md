# Erase.bg: Get Transformation Modules

Retrieves transformation modules from Erase.bg.

```
GET https://connect.mindcloud.co/v1/universal/erasebg/latest/actions/get-transformation-modules
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Erase.bg `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/erasebg/latest/actions/get-transformation-modules?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/erasebg/latest/actions/get-transformation-modules?${params}`, {
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
      "delimiters": {
        "operationSeparator": "string",
        "parameterSeparator": "string"
      },
      "plugins": {},
      "presets": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `delimiters` | object |  |
| `delimiters.operationSeparator` | string |  |
| `delimiters.parameterSeparator` | string |  |
| `plugins` | object |  |
| `presets` | array<object> |  |

## Native endpoint

Through the native Erase.bg API, this operation is `GET /service/platform/assets/v1.0/playground/plugins` (base URL `https://api.pixelbin.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-transformation-modules.md) for the provider-specific parameters and requirements.

