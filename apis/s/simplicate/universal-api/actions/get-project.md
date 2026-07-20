# Simplicate: Get Project



```
GET https://connect.mindcloud.co/v1/universal/simplicate/latest/actions/get-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Simplicate `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/simplicate/latest/actions/get-project?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/simplicate/latest/actions/get-project?${params}`, {
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
| `id` | string | yes | The project id |

## Response

```json
{
  "success": true,
  "data": [
    {
      "billable": true,
      "budget": {
        "costs": {
          "valueBudget": 1,
          "valueSpent": 1
        },
        "hours": {
          "amountSpent": 1,
          "valueSpent": 1
        },
        "total": {
          "valueBudget": 1,
          "valueInvoiced": 1,
          "valueSpent": 1
        }
      },
      "canRegisterMileage": true,
      "created": "string",
      "createdAt": "string",
      "hoursRateType": "string",
      "id": "string",
      "isInvoiceApproval": true,
      "isReverseBilling": true,
      "modified": "string",
      "myOrganizationProfile": {
        "id": "string",
        "organization": {
          "id": "string",
          "name": "Ava Chen"
        }
      },
      "myOrganizationProfileId": "string",
      "name": "Ava Chen",
      "note": "string",
      "organization": {
        "id": "string",
        "name": "Ava Chen"
      },
      "organizationId": "string",
      "projectStatus": {
        "id": "string",
        "label": "string"
      },
      "separateInvoiceRecipient": {
        "isSeparateInvoiceRecipient": true
      },
      "simplicateUrl": "https://example.com",
      "timelineEmailAddress": "ava@example.com",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `billable` | boolean |  |
| `budget.costs.valueBudget` | number |  |
| `budget.costs.valueSpent` | number |  |
| `budget.hours.amountSpent` | number |  |
| `budget.hours.valueSpent` | number |  |
| `budget.total.valueBudget` | number |  |
| `budget.total.valueInvoiced` | number |  |
| `budget.total.valueSpent` | number |  |
| `canRegisterMileage` | boolean |  |
| `created` | string |  |
| `createdAt` | string |  |
| `hoursRateType` | string |  |
| `id` | string |  |
| `isInvoiceApproval` | boolean |  |
| `isReverseBilling` | boolean |  |
| `modified` | string |  |
| `myOrganizationProfile.id` | string |  |
| `myOrganizationProfile.organization.id` | string |  |
| `myOrganizationProfile.organization.name` | string |  |
| `myOrganizationProfileId` | string |  |
| `name` | string |  |
| `note` | string |  |
| `organization.id` | string |  |
| `organization.name` | string |  |
| `organizationId` | string |  |
| `projectStatus.id` | string |  |
| `projectStatus.label` | string |  |
| `separateInvoiceRecipient.isSeparateInvoiceRecipient` | boolean |  |
| `simplicateUrl` | string |  |
| `timelineEmailAddress` | string |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Simplicate API, this operation is `GET /projects/project/:id` (base URL `https://{{credentials.subdomain}}/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-project.md) for the provider-specific parameters and requirements.

