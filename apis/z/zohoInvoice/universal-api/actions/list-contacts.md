# Zoho Invoice: List Contacts

Retrieves contacts from Zoho Invoice.

```
GET https://connect.mindcloud.co/v1/universal/zohoInvoice/latest/actions/list-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Invoice `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoInvoice/latest/actions/list-contacts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoInvoice/latest/actions/list-contacts?${params}`, {
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
| `searchText` | string | no | Search contacts by contact name or notes. Example: `Acme`. |
| `contactName` | string | no | Search contacts by contact name. Example: `Acme Corp`. |
| `companyName` | string | no | Search contacts by company name. Example: `Acme Corp`. |
| `firstName` | string | no | Search contacts by first name of the contact person. Example: `Jane`. |
| `lastName` | string | no | Search contacts by last name of the contact person. Example: `Doe`. |
| `email` | string | no | Search contacts by email ID of the contact person. Example: `jane@example.com`. |
| `phone` | string | no | Search contacts by phone number of the contact person. Example: `5551231234`. |
| `address` | string | no | Search contacts by any of the address fields. Example: `Pleasanton`. |
| `filterBy` | list<string> | no | Filter contacts by status. One of: `Status.Active`, `Status.All`, `Status.Crm`, `Status.Duplicate`, `Status.Inactive`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contactNameStartswith` | string | no | Variant of contact_name. Example: `Acme`. |
| `contactNameContains` | string | no | Variant of contact_name. Example: `Acme`. |
| `companyNameStartswith` | string | no | Variant of company_name. Example: `Acme`. |
| `companyNameContains` | string | no | Variant of company_name. Example: `Acme`. |
| `firstNameStartswith` | string | no | Variant of first_name. Example: `Ja`. |
| `firstNameContains` | string | no | Variant of first_name. Example: `ane`. |
| `lastNameStartswith` | string | no | Variant of last_name. Example: `Do`. |
| `lastNameContains` | string | no | Variant of last_name. Example: `oe`. |
| `phoneStartswith` | string | no | Variant of phone. Example: `555`. |
| `phoneContains` | string | no | Variant of phone. Example: `123`. |
| `addressStartswith` | string | no | Variant of address. Example: `Pleas`. |
| `addressContains` | string | no | Variant of address. Example: `asant`. |
| `zcrmContactId` | string | no | CRM Contact ID for the contact. Example: `1234567890`. |
| `zcrmAccountId` | string | no | CRM Account ID for the contact. Example: `1234567890`. |

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

Through the native Zoho Invoice API, this operation is `GET /contacts` (base URL `https://www.zohoapis.com/invoice/v3`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-contacts.md) for the provider-specific parameters and requirements.

