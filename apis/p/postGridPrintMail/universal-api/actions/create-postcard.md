# PostGrid Print & Mail: Create Postcard

Creates a postcard in PostGrid Print & Mail.

```
POST https://connect.mindcloud.co/v1/universal/postGridPrintMail/latest/actions/create-postcard
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PostGrid Print & Mail `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/postGridPrintMail/latest/actions/create-postcard" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "to": "string",
  "size": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/postGridPrintMail/latest/actions/create-postcard', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "to": "string",
    "size": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `to` | string | yes | The recipient contact ID or recipient payload. |
| `size` | string | yes | The postcard size. |
| `frontHTML` | string | no | Inline HTML for the front of the postcard. |
| `backHTML` | string | no | Inline HTML for the back of the postcard. |
| `frontTemplate` | string | no | The template ID for the front of the postcard. |
| `backTemplate` | string | no | The template ID for the back of the postcard. |
| `pdf` | string | no | A two-page PDF source for the postcard. |
| `from` | string | no | The sender contact ID or sender payload. |
| `mergeVariables` | object | no | Template merge variables for the postcard. |
| `description` | string | no | An optional description visible in the API and dashboard. |
| `metadata` | object | no | Custom metadata for this postcard. |
| `sendDate` | date | no | Schedule the postcard for a future send date. |
| `mailingClass` | string | no | The mailing class for the postcard. |
| `paper` | string | no | Paper stock settings for the postcard. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "backHTML": "string",
      "cancellation": {},
      "carrierTracking": {},
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "frontHTML": "string",
      "id": "string",
      "live": true,
      "mailingClass": "string",
      "object": "string",
      "pageCount": 1,
      "paper": "string",
      "sendDate": "2026-05-07T12:00:00.000Z",
      "size": "string",
      "status": "string",
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
| `backHTML` | string |  |
| `cancellation` | object |  |
| `carrierTracking` | object |  |
| `createdAt` | date |  |
| `description` | string |  |
| `frontHTML` | string |  |
| `id` | string |  |
| `live` | boolean |  |
| `mailingClass` | string |  |
| `object` | string |  |
| `pageCount` | number |  |
| `paper` | string |  |
| `sendDate` | date |  |
| `size` | string |  |
| `status` | string |  |
| `to` | object |  |
| `updatedAt` | date |  |
| `url` | string |  |

## Native endpoint

Through the native PostGrid Print & Mail API, this operation is `POST /postcards` (base URL `https://api.postgrid.com/print-mail/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-postcard.md) for the provider-specific parameters and requirements.

