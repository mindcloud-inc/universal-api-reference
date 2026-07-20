# ConvertHub: Get Format Conversions

Retrieves supported target formats for a source format in ConvertHub.

```
GET https://connect.mindcloud.co/v1/universal/convertHub/latest/actions/get-format-conversions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ConvertHub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/convertHub/latest/actions/get-format-conversions?connectionId=$CONNECTION_ID&format=png" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "format": "png"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/convertHub/latest/actions/get-format-conversions?${params}`, {
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
| `format` | string | yes | Example: `png`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "available_conversions": {
        "mime_type": "string",
        "target_format": "string"
      },
      "mime_type": "string",
      "source_format": "string",
      "success": true,
      "total_conversions": 1,
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `available_conversions` | array<object> |  |
| `available_conversions.mime_type` | string |  |
| `available_conversions.target_format` | string |  |
| `mime_type` | string |  |
| `source_format` | string |  |
| `success` | boolean |  |
| `total_conversions` | number |  |
| `type` | string |  |

## Native endpoint

Through the native ConvertHub API, this operation is `GET /v2/formats/:format/conversions` (base URL `https://api.converthub.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-format-conversions.md) for the provider-specific parameters and requirements.

