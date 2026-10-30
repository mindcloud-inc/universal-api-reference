# GoCanvas: Retrieve Basic Form PDF



```
GET https://connect.mindcloud.co/v1/universal/goCanvas/latest/actions/retrieve-basic-form-pdf
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GoCanvas `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/goCanvas/latest/actions/retrieve-basic-form-pdf?connectionId=$CONNECTION_ID&formId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "formId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/goCanvas/latest/actions/retrieve-basic-form-pdf?${params}`, {
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
| `formId` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "base64": "string",
      "formId": 1,
      "id": 1,
      "type": "string",
      "virusScanComplete": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `base64` | string |  |
| `formId` | number |  |
| `id` | number |  |
| `type` | string |  |
| `virusScanComplete` | boolean |  |

## Native endpoint

Through the native GoCanvas API, this operation is `GET /forms/:formId/basic_pdf` (base URL `https://www.gocanvas.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-basic-form-pdf.md) for the provider-specific parameters and requirements.

