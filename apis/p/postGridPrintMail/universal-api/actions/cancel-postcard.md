# PostGrid Print & Mail: Cancel Postcard

Cancels a postcard in PostGrid Print & Mail.

```
DELETE https://connect.mindcloud.co/v1/universal/postGridPrintMail/latest/actions/cancel-postcard
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PostGrid Print & Mail `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/postGridPrintMail/latest/actions/cancel-postcard?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/postGridPrintMail/latest/actions/cancel-postcard?${params}`, {
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

Through the native PostGrid Print & Mail API, this operation is `DELETE /postcards/{{id}}` (base URL `https://api.postgrid.com/print-mail/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/cancel-postcard.md) for the provider-specific parameters and requirements.

