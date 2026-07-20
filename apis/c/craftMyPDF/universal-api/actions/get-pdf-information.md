# CraftMyPDF: Get PDF Information

Retrieves PDF file information from CraftMyPDF.

```
GET https://connect.mindcloud.co/v1/universal/craftMyPDF/latest/actions/get-pdf-information
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CraftMyPDF `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/craftMyPDF/latest/actions/get-pdf-information?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/craftMyPDF/latest/actions/get-pdf-information?${params}`, {
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
| `url` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "creationDate": "2026-05-07T12:00:00.000Z",
      "creator": "string",
      "modificationDate": "2026-05-07T12:00:00.000Z",
      "producer": "string",
      "status": "string",
      "totalPages": 1,
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `creationDate` | date |  |
| `creator` | string |  |
| `modificationDate` | date |  |
| `producer` | string |  |
| `status` | string |  |
| `totalPages` | number |  |
| `url` | string |  |

## Native endpoint

Through the native CraftMyPDF API, this operation is `GET /get-pdf-info` (base URL `https://api.craftmypdf.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-pdf-information.md) for the provider-specific parameters and requirements.

