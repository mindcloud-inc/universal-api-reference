# PostGrid Print & Mail: Get Cheque

Retrieves a cheque from PostGrid Print & Mail.

```
GET https://connect.mindcloud.co/v1/universal/postGridPrintMail/latest/actions/get-cheque
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PostGrid Print & Mail `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/postGridPrintMail/latest/actions/get-cheque?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/postGridPrintMail/latest/actions/get-cheque?${params}`, {
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
      "amount": 1,
      "bankAccount": "string",
      "cancellation": {},
      "carrierTracking": {},
      "createdAt": "2026-05-07T12:00:00.000Z",
      "currencyCode": "string",
      "description": "string",
      "envelope": "string",
      "from": {},
      "id": "string",
      "live": true,
      "mailingClass": "string",
      "number": 1,
      "object": "string",
      "pageCount": 1,
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
| `amount` | number |  |
| `bankAccount` | string |  |
| `cancellation` | object |  |
| `carrierTracking` | object |  |
| `createdAt` | date |  |
| `currencyCode` | string |  |
| `description` | string |  |
| `envelope` | string |  |
| `from` | object |  |
| `id` | string |  |
| `live` | boolean |  |
| `mailingClass` | string |  |
| `number` | number |  |
| `object` | string |  |
| `pageCount` | number |  |
| `sendDate` | date |  |
| `size` | string |  |
| `status` | string |  |
| `to` | object |  |
| `updatedAt` | date |  |
| `url` | string |  |

## Native endpoint

Through the native PostGrid Print & Mail API, this operation is `GET /cheques/{{id}}` (base URL `https://api.postgrid.com/print-mail/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-cheque.md) for the provider-specific parameters and requirements.

