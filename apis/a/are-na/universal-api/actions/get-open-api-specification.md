# Are.na: Get OpenAPI Specification

Retrieves the OpenAPI specification from Are.na.

```
GET https://connect.mindcloud.co/v1/universal/are-na/latest/actions/get-open-api-specification
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Are.na `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/are-na/latest/actions/get-open-api-specification?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/are-na/latest/actions/get-open-api-specification?${params}`, {
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
      "components": {},
      "info": {},
      "openapi": "string",
      "paths": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `components` | object |  |
| `info` | object |  |
| `openapi` | string |  |
| `paths` | object |  |

## Native endpoint

Through the native Are.na API, this operation is `GET openapi.json` (base URL `https://api.are.na/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-open-api-specification.md) for the provider-specific parameters and requirements.

