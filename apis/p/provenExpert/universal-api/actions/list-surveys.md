# ProvenExpert: List Surveys

Lists your surveys in ProvenExpert.

```
GET https://connect.mindcloud.co/v1/universal/provenExpert/latest/actions/list-surveys
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ProvenExpert `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/provenExpert/latest/actions/list-surveys?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/provenExpert/latest/actions/list-surveys?${params}`, {
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
      "active": 1,
      "code": "string",
      "created": 1,
      "name": "Ava Chen",
      "pos": 1,
      "printPdf": "string",
      "printPng": "string",
      "qr": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | number | Survey active flag. |
| `code` | string | Survey code returned by ProvenExpert. |
| `created` | number | Unix timestamp for when the survey was created. |
| `name` | string | Survey display name. |
| `pos` | number | Survey position index. |
| `printPdf` | string | Printable PDF output URL. |
| `printPng` | string | Printable PNG output URL. |
| `qr` | string | QR code image URL for the survey. |
| `url` | string | Survey landing page URL. |

## Native endpoint

Through the native ProvenExpert API, this operation is `POST /survey/get` (base URL `https://www.provenexpert.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-surveys.md) for the provider-specific parameters and requirements.

