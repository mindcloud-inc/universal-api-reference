# ConvertHub: Check Conversion Support

Checks whether ConvertHub supports a specific format conversion.

```
GET https://connect.mindcloud.co/v1/universal/convertHub/latest/actions/check-conversion-support
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ConvertHub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/convertHub/latest/actions/check-conversion-support?connectionId=$CONNECTION_ID&sourceFormat=docx&targetFormat=pdf" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "sourceFormat": "docx",
  "targetFormat": "pdf"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/convertHub/latest/actions/check-conversion-support?${params}`, {
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
| `sourceFormat` | string | yes | Example: `docx`. |
| `targetFormat` | string | yes | Example: `pdf`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "source_format": {
        "extension": "string",
        "mime_type": "string",
        "type": "string"
      },
      "success": true,
      "supported": true,
      "target_format": {
        "extension": "string",
        "mime_type": "string",
        "type": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `source_format` | object |  |
| `source_format.extension` | string |  |
| `source_format.mime_type` | string |  |
| `source_format.type` | string |  |
| `success` | boolean |  |
| `supported` | boolean |  |
| `target_format` | object |  |
| `target_format.extension` | string |  |
| `target_format.mime_type` | string |  |
| `target_format.type` | string |  |

## Native endpoint

Through the native ConvertHub API, this operation is `GET /v2/formats/:sourceFormat/to/:targetFormat` (base URL `https://api.converthub.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/check-conversion-support.md) for the provider-specific parameters and requirements.

