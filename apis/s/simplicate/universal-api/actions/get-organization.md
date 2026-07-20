# Simplicate: Get Organization



```
GET https://connect.mindcloud.co/v1/universal/simplicate/latest/actions/get-organization
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Simplicate `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/simplicate/latest/actions/get-organization?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/simplicate/latest/actions/get-organization?${params}`, {
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
| `id` | string | no | Organization id path parameter from the Simplicate get organization by id endpoint. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "allowAutocollect": "string",
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
        "sendEmailType": "ava@example.com",
        "sendInvoiceEmailToCc": true,
        "sendInvoiceEmailToContact": true,
        "sendInvoiceEmailToFixedEmail": true,
        "sendInvoiceEmailToProjectContact": true
      },
      "hasDifferentPostalAddress": true,
      "id": "string",
      "isActive": true,
      "modified": "string",
      "name": "Ava Chen",
      "note": "string",
      "simplicateUrl": "https://example.com",
      "timelineEmailAddress": "ava@example.com",
      "updatedAt": "string",
      "visitingAddress": {
        "country": "string",
        "countryCode": "string",
        "countryId": "string",
        "id": "string",
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
| `created` | string |  |
| `createdAt` | string |  |
| `debtor.attentionTo` | string |  |
| `debtor.autocollect` | boolean |  |
| `debtor.autosendSubscriptionInvoice` | boolean |  |
| `debtor.paymentTerm.days` | number |  |
| `debtor.paymentTerm.id` | string |  |
| `debtor.paymentTerm.method` | string |  |
| `debtor.paymentTerm.name` | string |  |
| `debtor.sendEmailType` | string |  |
| `debtor.sendInvoiceEmailToCc` | boolean |  |
| `debtor.sendInvoiceEmailToContact` | boolean |  |
| `debtor.sendInvoiceEmailToFixedEmail` | boolean |  |
| `debtor.sendInvoiceEmailToProjectContact` | boolean |  |
| `hasDifferentPostalAddress` | boolean |  |
| `id` | string |  |
| `isActive` | boolean |  |
| `modified` | string |  |
| `name` | string |  |
| `note` | string |  |
| `simplicateUrl` | string |  |
| `timelineEmailAddress` | string |  |
| `updatedAt` | string |  |
| `visitingAddress.country` | string |  |
| `visitingAddress.countryCode` | string |  |
| `visitingAddress.countryId` | string |  |
| `visitingAddress.id` | string |  |
| `visitingAddress.type` | string |  |

## Native endpoint

Through the native Simplicate API, this operation is `GET /crm/organization/:id` (base URL `https://{{credentials.subdomain}}/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-organization.md) for the provider-specific parameters and requirements.

