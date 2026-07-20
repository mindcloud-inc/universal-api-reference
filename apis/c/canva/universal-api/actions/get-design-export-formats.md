# Canva: Get Design Export Formats

Retrieves export formats for a Canva design.

```
GET https://connect.mindcloud.co/v1/universal/canva/latest/actions/get-design-export-formats
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Canva `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/canva/latest/actions/get-design-export-formats?connectionId=$CONNECTION_ID&designId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "designId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/canva/latest/actions/get-design-export-formats?${params}`, {
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
| `designId` | string | yes | The Canva design ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "gif": {},
      "jpg": {},
      "mp4": {},
      "pdf": {},
      "png": {},
      "pptx": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `gif` | object |  |
| `jpg` | object |  |
| `mp4` | object |  |
| `pdf` | object |  |
| `png` | object |  |
| `pptx` | object |  |

## Native endpoint

Through the native Canva API, this operation is `GET /v1/designs/:designId/export-formats` (base URL `https://api.canva.com/rest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-design-export-formats.md) for the provider-specific parameters and requirements.

