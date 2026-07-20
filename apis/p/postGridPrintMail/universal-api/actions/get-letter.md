# PostGrid Print & Mail: Get Letter

Retrieves a letter from PostGrid Print & Mail.

```
GET https://connect.mindcloud.co/v1/universal/postGridPrintMail/latest/actions/get-letter
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PostGrid Print & Mail `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/postGridPrintMail/latest/actions/get-letter?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/postGridPrintMail/latest/actions/get-letter?${params}`, {
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
| `id` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "addressPlacement": "string",
      "attachedPDF": {},
      "cancellation": {},
      "carrierTracking": {},
      "color": true,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "doubleSided": true,
      "envelope": "string",
      "envelopeType": "string",
      "from": {},
      "html": "string",
      "id": "string",
      "live": true,
      "mailingClass": "string",
      "object": "string",
      "pageCount": 1,
      "sendDate": "2026-05-07T12:00:00.000Z",
      "size": "string",
      "status": "string",
      "template": "string",
      "to": {},
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `addressPlacement` | string |  |
| `attachedPDF` | object |  |
| `cancellation` | object |  |
| `carrierTracking` | object |  |
| `color` | boolean |  |
| `createdAt` | date |  |
| `description` | string |  |
| `doubleSided` | boolean |  |
| `envelope` | string |  |
| `envelopeType` | string |  |
| `from` | object |  |
| `html` | string |  |
| `id` | string |  |
| `live` | boolean |  |
| `mailingClass` | string |  |
| `object` | string |  |
| `pageCount` | number |  |
| `sendDate` | date |  |
| `size` | string |  |
| `status` | string |  |
| `template` | string |  |
| `to` | object |  |
| `updatedAt` | date |  |
| `url` | string |  |

## Native endpoint

Through the native PostGrid Print & Mail API, this operation is `GET /letters/{{id}}` (base URL `https://api.postgrid.com/print-mail/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-letter.md) for the provider-specific parameters and requirements.

