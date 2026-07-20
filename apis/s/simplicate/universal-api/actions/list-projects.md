# Simplicate: List Projects



```
GET https://connect.mindcloud.co/v1/universal/simplicate/latest/actions/list-projects
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Simplicate `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/simplicate/latest/actions/list-projects?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/simplicate/latest/actions/list-projects?${params}`, {
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
      "billable": true,
      "budget": {
        "costs": {
          "valueBudget": 1,
          "valueSpent": 1
        },
        "hours": {
          "amountBudget": 1,
          "amountSpent": 1,
          "valueBudget": 1,
          "valueSpent": 1
        },
        "total": {
          "valueBudget": 1,
          "valueInvoiced": 1,
          "valueSpent": 1
        }
      },
      "canRegisterMileage": true,
      "contact": {
        "id": "string",
        "organization": {
          "id": "string",
          "name": "Ava Chen"
        },
        "person": {
          "fullName": "Ava Chen",
          "id": "string"
        }
      },
      "contactId": "string",
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
      "organization": {
        "id": "string",
        "name": "Ava Chen"
      },
      "organizationId": "string",
      "projectManager": {
        "employeeId": "string",
        "id": "string",
        "name": "Ava Chen",
        "personId": "string"
      },
      "projectNumber": "string",
      "projectStatus": {
        "id": "string",
        "label": "string"
      },
      "separateInvoiceRecipient": {
        "isSeparateInvoiceRecipient": true
      },
      "simplicateUrl": "https://example.com",
      "startDate": "string",
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
| `budget.hours.amountBudget` | number |  |
| `budget.hours.amountSpent` | number |  |
| `budget.hours.valueBudget` | number |  |
| `budget.hours.valueSpent` | number |  |
| `budget.total.valueBudget` | number |  |
| `budget.total.valueInvoiced` | number |  |
| `budget.total.valueSpent` | number |  |
| `canRegisterMileage` | boolean |  |
| `contact.id` | string |  |
| `contact.organization.id` | string |  |
| `contact.organization.name` | string |  |
| `contact.person.fullName` | string |  |
| `contact.person.id` | string |  |
| `contactId` | string |  |
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
| `organization.id` | string |  |
| `organization.name` | string |  |
| `organizationId` | string |  |
| `projectManager.employeeId` | string |  |
| `projectManager.id` | string |  |
| `projectManager.name` | string |  |
| `projectManager.personId` | string |  |
| `projectNumber` | string |  |
| `projectStatus.id` | string |  |
| `projectStatus.label` | string |  |
| `separateInvoiceRecipient.isSeparateInvoiceRecipient` | boolean |  |
| `simplicateUrl` | string |  |
| `startDate` | string |  |
| `timelineEmailAddress` | string |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Simplicate API, this operation is `GET /projects/project` (base URL `https://{{credentials.subdomain}}/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-projects.md) for the provider-specific parameters and requirements.

