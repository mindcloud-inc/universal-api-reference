# Simplicate: List Organizations



```
GET https://connect.mindcloud.co/v1/universal/simplicate/latest/actions/list-organizations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Simplicate `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/simplicate/latest/actions/list-organizations?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/simplicate/latest/actions/list-organizations?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "allowAutocollect": "string",
      "cocCode": "string",
      "created": "string",
      "createdAt": "string",
      "debtor": {
        "attentionTo": "string",
        "autocollect": true,
        "autosendSubscriptionInvoice": true,
        "paymentTerm": {
          "days": 1,
          "id": "string",
          "method": "string",
          "name": "Ava Chen"
        },
        "provisionMethod": "string",
        "sendEmailType": "ava@example.com",
        "sendInvoiceEmailToCc": true,
        "sendInvoiceEmailToContact": true,
        "sendInvoiceEmailToFixedEmail": true,
        "sendInvoiceEmailToProjectContact": true
      },
      "email": "ava@example.com",
      "hasDifferentPostalAddress": true,
      "id": "string",
      "industry": {
        "id": "string",
        "name": "Ava Chen"
      },
      "isActive": true,
      "linkedinUrl": "https://example.com",
      "linkedPersonsContacts": [
        {
          "familyName": "https://example.com",
          "familyNamePrefix": "https://example.com",
          "firstName": "https://example.com",
          "id": "https://example.com",
          "isActive": true,
          "personId": "https://example.com",
          "workEmail": "ava@example.com",
          "workFunction": "https://example.com",
          "workMobile": "https://example.com"
        }
      ],
      "modified": "string",
      "name": "Ava Chen",
      "note": "string",
      "phone": "string",
      "relationManager": {
        "id": "string",
        "name": "Ava Chen"
      },
      "relationType": {
        "color": "string",
        "id": "string",
        "label": "string"
      },
      "simplicateUrl": "https://example.com",
      "timelineEmailAddress": "ava@example.com",
      "updatedAt": "string",
      "url": "https://example.com",
      "visitingAddress": {
        "country": "string",
        "countryCode": "string",
        "countryId": "string",
        "id": "string",
        "line1": "string",
        "locality": "string",
        "postalCode": "string",
        "type": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `allowAutocollect` | string |  |
| `cocCode` | string |  |
| `created` | string |  |
| `createdAt` | string |  |
| `debtor.attentionTo` | string |  |
| `debtor.autocollect` | boolean |  |
| `debtor.autosendSubscriptionInvoice` | boolean |  |
| `debtor.paymentTerm.days` | number |  |
| `debtor.paymentTerm.id` | string |  |
| `debtor.paymentTerm.method` | string |  |
| `debtor.paymentTerm.name` | string |  |
| `debtor.provisionMethod` | string |  |
| `debtor.sendEmailType` | string |  |
| `debtor.sendInvoiceEmailToCc` | boolean |  |
| `debtor.sendInvoiceEmailToContact` | boolean |  |
| `debtor.sendInvoiceEmailToFixedEmail` | boolean |  |
| `debtor.sendInvoiceEmailToProjectContact` | boolean |  |
| `email` | string |  |
| `hasDifferentPostalAddress` | boolean |  |
| `id` | string |  |
| `industry.id` | string |  |
| `industry.name` | string |  |
| `isActive` | boolean |  |
| `linkedinUrl` | string |  |
| `linkedPersonsContacts[].familyName` | string |  |
| `linkedPersonsContacts[].familyNamePrefix` | string |  |
| `linkedPersonsContacts[].firstName` | string |  |
| `linkedPersonsContacts[].id` | string |  |
| `linkedPersonsContacts[].isActive` | boolean |  |
| `linkedPersonsContacts[].personId` | string |  |
| `linkedPersonsContacts[].workEmail` | string |  |
| `linkedPersonsContacts[].workFunction` | string |  |
| `linkedPersonsContacts[].workMobile` | string |  |
| `modified` | string |  |
| `name` | string |  |
| `note` | string |  |
| `phone` | string |  |
| `relationManager.id` | string |  |
| `relationManager.name` | string |  |
| `relationType.color` | string |  |
| `relationType.id` | string |  |
| `relationType.label` | string |  |
| `simplicateUrl` | string |  |
| `timelineEmailAddress` | string |  |
| `updatedAt` | string |  |
| `url` | string |  |
| `visitingAddress.country` | string |  |
| `visitingAddress.countryCode` | string |  |
| `visitingAddress.countryId` | string |  |
| `visitingAddress.id` | string |  |
| `visitingAddress.line1` | string |  |
| `visitingAddress.locality` | string |  |
| `visitingAddress.postalCode` | string |  |
| `visitingAddress.type` | string |  |

## Native endpoint

Through the native Simplicate API, this operation is `GET /crm/organization` (base URL `https://{{credentials.subdomain}}/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-organizations.md) for the provider-specific parameters and requirements.

