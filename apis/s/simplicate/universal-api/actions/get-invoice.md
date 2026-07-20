# Simplicate: Get Invoice



```
GET https://connect.mindcloud.co/v1/universal/simplicate/latest/actions/get-invoice
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Simplicate `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/simplicate/latest/actions/get-invoice?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/simplicate/latest/actions/get-invoice?${params}`, {
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
| `id` | string | yes | Invoice identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "comments": "string",
      "compositionType": "string",
      "contactId": "string",
      "created": "string",
      "createdAt": "string",
      "date": "string",
      "id": "string",
      "invoiceLines": [
        {
          "amount": "string",
          "date": "string",
          "description": "string",
          "id": "string",
          "isAdvanceDeposit": "string",
          "price": "string",
          "revenueGroup": {
            "id": "string",
            "label": "string"
          },
          "totalVat": "string",
          "vatClass": {
            "code": "string",
            "id": "string",
            "label": "string",
            "percentage": "string"
          }
        }
      ],
      "isCreditInvoice": true,
      "myOrganizationProfile": {
        "id": "string",
        "organization": {
          "id": "string",
          "name": "Ava Chen"
        }
      },
      "myOrganizationProfileId": "string",
      "organization": {
        "id": "string",
        "name": "Ava Chen"
      },
      "organizationId": "string",
      "paymentTerm": {
        "days": "string",
        "id": "string",
        "name": "Ava Chen"
      },
      "reminder": {
        "nextAction": "string",
        "paused": true
      },
      "sendingMethod": "string",
      "simplicateUrl": "https://example.com",
      "status": {
        "id": "string",
        "name": "Ava Chen"
      },
      "subject": "string",
      "timelineEmailAddress": "ava@example.com",
      "totalExcludingVat": 1,
      "totalIncludingVat": 1,
      "totalOutstanding": 1,
      "totalVat": 1,
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `comments` | string |  |
| `compositionType` | string |  |
| `contactId` | string |  |
| `created` | string |  |
| `createdAt` | string |  |
| `date` | string |  |
| `id` | string |  |
| `invoiceLines[].amount` | string |  |
| `invoiceLines[].date` | string |  |
| `invoiceLines[].description` | string |  |
| `invoiceLines[].id` | string |  |
| `invoiceLines[].isAdvanceDeposit` | string |  |
| `invoiceLines[].price` | string |  |
| `invoiceLines[].revenueGroup.id` | string |  |
| `invoiceLines[].revenueGroup.label` | string |  |
| `invoiceLines[].totalVat` | string |  |
| `invoiceLines[].vatClass.code` | string |  |
| `invoiceLines[].vatClass.id` | string |  |
| `invoiceLines[].vatClass.label` | string |  |
| `invoiceLines[].vatClass.percentage` | string |  |
| `isCreditInvoice` | boolean |  |
| `myOrganizationProfile.id` | string |  |
| `myOrganizationProfile.organization.id` | string |  |
| `myOrganizationProfile.organization.name` | string |  |
| `myOrganizationProfileId` | string |  |
| `organization.id` | string |  |
| `organization.name` | string |  |
| `organizationId` | string |  |
| `paymentTerm.days` | string |  |
| `paymentTerm.id` | string |  |
| `paymentTerm.name` | string |  |
| `reminder.nextAction` | string |  |
| `reminder.paused` | boolean |  |
| `sendingMethod` | string |  |
| `simplicateUrl` | string |  |
| `status.id` | string |  |
| `status.name` | string |  |
| `subject` | string |  |
| `timelineEmailAddress` | string |  |
| `totalExcludingVat` | number |  |
| `totalIncludingVat` | number |  |
| `totalOutstanding` | number |  |
| `totalVat` | number |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Simplicate API, this operation is `GET /invoices/invoice/:id` (base URL `https://{{credentials.subdomain}}/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-invoice.md) for the provider-specific parameters and requirements.

