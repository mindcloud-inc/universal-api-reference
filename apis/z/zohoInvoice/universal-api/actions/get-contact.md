# Zoho Invoice: Get Contact

Retrieves a contact from Zoho Invoice.

```
GET https://connect.mindcloud.co/v1/universal/zohoInvoice/latest/actions/get-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Invoice `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoInvoice/latest/actions/get-contact?connectionId=$CONNECTION_ID&contactId=460000000026049" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "contactId": "460000000026049"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoInvoice/latest/actions/get-contact?${params}`, {
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
| `contactId` | string | yes | Unique identifier of the contact. Example: `460000000026049`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "companyName": "Ava Chen",
      "contactId": "string",
      "contactName": "Ava Chen",
      "contactType": "string",
      "createdTime": "2026-05-07T12:00:00.000Z",
      "currencyCode": "string",
      "customerName": "Ava Chen",
      "customerSubType": "string",
      "email": "ava@example.com",
      "hasAttachment": true,
      "lastModifiedTime": "2026-05-07T12:00:00.000Z",
      "mobile": "string",
      "phone": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `companyName` | string |  |
| `contactId` | string |  |
| `contactName` | string |  |
| `contactType` | string |  |
| `createdTime` | date |  |
| `currencyCode` | string |  |
| `customerName` | string |  |
| `customerSubType` | string |  |
| `email` | string |  |
| `hasAttachment` | boolean |  |
| `lastModifiedTime` | date |  |
| `mobile` | string |  |
| `phone` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Zoho Invoice API, this operation is `GET /contacts/:contact_id` (base URL `https://www.zohoapis.com/invoice/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-contact.md) for the provider-specific parameters and requirements.

