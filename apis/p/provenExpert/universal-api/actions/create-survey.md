# ProvenExpert: Create Survey

Creates a survey in ProvenExpert.

```
POST https://connect.mindcloud.co/v1/universal/provenExpert/latest/actions/create-survey
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ProvenExpert `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/provenExpert/latest/actions/create-survey" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "data.name": "MindCloud Wizard Survey"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/provenExpert/latest/actions/create-survey', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "data.name": "MindCloud Wizard Survey"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `data.name` | string | yes | Name of the survey to create. Example: `MindCloud Wizard Survey`. |
| `data.pos` | number | no | Whether the survey should be created as a point-of-sale survey. Example: `0`. |

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
| `active` | number | Whether the survey is active. |
| `code` | string | Survey code returned by ProvenExpert. |
| `created` | number | Unix timestamp for when the survey was created. |
| `name` | string | Survey display name. |
| `pos` | number | Survey ordering position. |
| `printPdf` | string | Printable PDF asset URL. |
| `printPng` | string | Printable PNG asset URL. |
| `qr` | string | QR code image URL for the survey. |
| `url` | string | Public survey URL. |

## Native endpoint

Through the native ProvenExpert API, this operation is `POST /survey/create` (base URL `https://www.provenexpert.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-survey.md) for the provider-specific parameters and requirements.

