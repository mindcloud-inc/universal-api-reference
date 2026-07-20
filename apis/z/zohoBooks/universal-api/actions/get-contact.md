# Zoho Books: Get Contact



```
GET https://connect.mindcloud.co/v1/universal/zohoBooks/latest/actions/get-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Books `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoBooks/latest/actions/get-contact?connectionId=$CONNECTION_ID&contactId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "contactId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoBooks/latest/actions/get-contact?${params}`, {
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
| `contactId` | string | yes | Unique identifier of the contact. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "achSupported": true,
      "billingAddress": {},
      "companyName": "Ava Chen",
      "contactId": "string",
      "contactName": "Ava Chen",
      "contactPersons": [
        {}
      ],
      "contactType": "string",
      "createdDate": "string",
      "createdTime": "2026-05-07T12:00:00.000Z",
      "currencyCode": "string",
      "currencySymbol": "string",
      "customerSubType": "string",
      "customFieldHash": {},
      "customFields": [
        {}
      ],
      "email": "ava@example.com",
      "lastModifiedTime": "2026-05-07T12:00:00.000Z",
      "mobile": "string",
      "notes": "string",
      "paymentTerms": 1,
      "paymentTermsLabel": "string",
      "phone": "string",
      "salesChannel": "string",
      "shippingAddress": {},
      "status": "string",
      "tags": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `achSupported` | boolean |  |
| `billingAddress` | object |  |
| `companyName` | string |  |
| `contactId` | string |  |
| `contactName` | string |  |
| `contactPersons` | array<object> |  |
| `contactType` | string |  |
| `createdDate` | string |  |
| `createdTime` | date |  |
| `currencyCode` | string |  |
| `currencySymbol` | string |  |
| `customerSubType` | string |  |
| `customFieldHash` | object |  |
| `customFields` | array<object> |  |
| `email` | string |  |
| `lastModifiedTime` | date |  |
| `mobile` | string |  |
| `notes` | string |  |
| `paymentTerms` | number |  |
| `paymentTermsLabel` | string |  |
| `phone` | string |  |
| `salesChannel` | string |  |
| `shippingAddress` | object |  |
| `status` | string |  |
| `tags` | array<object> |  |

## Native endpoint

Through the native Zoho Books API, this operation is `GET /contacts/:contact_id` (base URL `https://www.zohoapis.com/books/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-contact.md) for the provider-specific parameters and requirements.

