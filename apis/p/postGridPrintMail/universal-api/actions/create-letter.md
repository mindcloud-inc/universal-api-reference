# PostGrid Print & Mail: Create Letter

Creates a letter in PostGrid Print & Mail.

```
POST https://connect.mindcloud.co/v1/universal/postGridPrintMail/latest/actions/create-letter
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PostGrid Print & Mail `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/postGridPrintMail/latest/actions/create-letter" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "to": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/postGridPrintMail/latest/actions/create-letter', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "to": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `to` | string | yes | The recipient contact ID or recipient payload. |
| `from` | string | no | The sender contact ID or sender payload. |
| `html` | string | no | Inline HTML content for the letter. |
| `template` | string | no | The PostGrid template ID to use for the letter. |
| `pdf` | string | no | A PDF URL or PDF source for the letter. |
| `mergeVariables` | object | no | Template merge variables for the letter. |
| `description` | string | no | An optional description visible in the API and dashboard. |
| `metadata` | object | no | Custom metadata for this letter. |
| `sendDate` | date | no | Schedule the letter for a future send date. |
| `mailingClass` | string | no | The mailing class for the letter. |
| `size` | string | no | The page size for the letter. |
| `addressPlacement` | string | no | How to place the address window content. |
| `doubleSided` | boolean | no | Print the letter double sided. |
| `color` | boolean | no | Print the letter in color. |
| `perforatedPage` | number | no | The page number to perforate for the letter. |
| `envelope` | string | no | Envelope settings for the letter. |
| `returnEnvelope` | string | no | The return-envelope configuration for the letter. |
| `attachedPDF` | object | no | Attach an additional PDF to the letter. |
| `plasticCard` | object | no | Plastic card settings for the letter. |

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

Through the native PostGrid Print & Mail API, this operation is `POST /letters` (base URL `https://api.postgrid.com/print-mail/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-letter.md) for the provider-specific parameters and requirements.

