# Extract Monster: Get API Info

Retrieves API information from Extract Monster.

```
GET https://connect.mindcloud.co/v1/universal/extractMonster/latest/actions/get-api-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Extract Monster `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/extractMonster/latest/actions/get-api-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/extractMonster/latest/actions/get-api-info?${params}`, {
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
      "description": "string",
      "endpoints": [
        "string"
      ],
      "message": "string",
      "supportedFormats": {},
      "version": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string | High-level API description. |
| `endpoints` | array<string> | Advertised API endpoints. |
| `message` | string | Service display name. |
| `supportedFormats` | object | Supported input formats grouped by media type. |
| `version` | string | Provider API version. |

## Native endpoint

Through the native Extract Monster API, this operation is `GET /` (base URL `https://api.extract.monster`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-api-info.md) for the provider-specific parameters and requirements.

