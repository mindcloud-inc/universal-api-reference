# Zoho Books: Update Contact



```
PUT https://connect.mindcloud.co/v1/universal/zohoBooks/latest/actions/update-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Books `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/zohoBooks/latest/actions/update-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contactId": "string",
  "contactName": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoBooks/latest/actions/update-contact', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contactId": "string",
    "contactName": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contactId` | string | yes | Unique identifier of the contact to update. |
| `contactName` | string | yes | Display name for the contact. |
| `contactType` | list | no | Determines whether the contact is a customer or vendor. One of: `customer`, `vendor`. |
| `companyName` | string | no | Legal or registered company name for the contact. |
| `website` | string | no | Official website URL of the contact. |
| `notes` | string | no | Additional notes about the contact. |
| `billingAddress` | object | no | Billing address information for the contact. |
| `billingAddress.address` | string | no | Street address line 1 for the billing address. |
| `billingAddress.city` | string | no | City for the billing address. |
| `billingAddress.state` | string | no | State for the billing address. |
| `billingAddress.zip` | string | no | Postal code for the billing address. |
| `billingAddress.country` | string | no | Country for the billing address. |
| `contactPersons[]` | array<object> | no | Contact people associated with the contact. |
| `contactPersons[].firstName` | string | no | First name of the contact person. |
| `contactPersons[].lastName` | string | no | Last name of the contact person. |
| `contactPersons[].email` | string | no | Email address of the contact person. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customerSubType` | list | no | Additional classification for customer contacts. One of: `business`, `individual`. |
| `creditLimit` | number | no | Maximum credit amount allowed for the customer. |
| `contactNumber` | string | no | Internal contact number. |
| `paymentTerms` | number | no | Number of days allowed for payment. |
| `contactPersons[].contactPersonId` | string | no | Unique identifier of an existing contact person. |

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

Through the native Zoho Books API, this operation is `PUT /contacts/:contact_id` (base URL `https://www.zohoapis.com/books/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-contact.md) for the provider-specific parameters and requirements.

