# Simplicate: List Hours



```
GET https://connect.mindcloud.co/v1/universal/simplicate/latest/actions/list-hours
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Simplicate `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/simplicate/latest/actions/list-hours?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/simplicate/latest/actions/list-hours?${params}`, {
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
      "absenceId": "string",
      "billable": true,
      "corrections": {
        "amount": 1,
        "lastCorrectionDate": "string",
        "value": 1
      },
      "createdAt": "string",
      "customFields": [
        {
          "filterable": true,
          "id": "string",
          "label": "string",
          "mandatory": true,
          "name": "Ava Chen",
          "position": 1,
          "renderType": "string",
          "searchable": true,
          "valueType": "string"
        }
      ],
      "durationInMinutes": 1,
      "employee": {
        "id": "string",
        "name": "Ava Chen"
      },
      "endDate": "string",
      "hours": 1,
      "id": "string",
      "isExternal": true,
      "isProductive": true,
      "isRecurring": true,
      "isTimeDefined": true,
      "leaveId": "string",
      "leaveStatus": {
        "id": "string",
        "label": "string"
      },
      "locked": true,
      "project": {
        "hasRegisterMileageEnabled": true,
        "id": "string",
        "name": "Ava Chen",
        "organization": {
          "id": "string",
          "name": "Ava Chen"
        },
        "projectNumber": "string"
      },
      "projectservice": {
        "defaultServiceId": "string",
        "id": "string",
        "name": "Ava Chen",
        "revenueGroupId": "string"
      },
      "shouldSyncToCronofy": true,
      "source": "string",
      "startDate": "string",
      "tariff": 1,
      "type": {
        "color": "string",
        "id": "string",
        "label": "string",
        "tariff": "string",
        "type": "string",
        "vatclass": {
          "id": "string",
          "label": "string",
          "percentage": 1
        }
      },
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `absenceId` | string |  |
| `billable` | boolean |  |
| `corrections.amount` | number |  |
| `corrections.lastCorrectionDate` | string |  |
| `corrections.value` | number |  |
| `createdAt` | string |  |
| `customFields[].filterable` | boolean |  |
| `customFields[].id` | string |  |
| `customFields[].label` | string |  |
| `customFields[].mandatory` | boolean |  |
| `customFields[].name` | string |  |
| `customFields[].position` | number |  |
| `customFields[].renderType` | string |  |
| `customFields[].searchable` | boolean |  |
| `customFields[].valueType` | string |  |
| `durationInMinutes` | number |  |
| `employee.id` | string |  |
| `employee.name` | string |  |
| `endDate` | string |  |
| `hours` | number |  |
| `id` | string |  |
| `isExternal` | boolean |  |
| `isProductive` | boolean |  |
| `isRecurring` | boolean |  |
| `isTimeDefined` | boolean |  |
| `leaveId` | string |  |
| `leaveStatus.id` | string |  |
| `leaveStatus.label` | string |  |
| `locked` | boolean |  |
| `project.hasRegisterMileageEnabled` | boolean |  |
| `project.id` | string |  |
| `project.name` | string |  |
| `project.organization.id` | string |  |
| `project.organization.name` | string |  |
| `project.projectNumber` | string |  |
| `projectservice.defaultServiceId` | string |  |
| `projectservice.id` | string |  |
| `projectservice.name` | string |  |
| `projectservice.revenueGroupId` | string |  |
| `shouldSyncToCronofy` | boolean |  |
| `source` | string |  |
| `startDate` | string |  |
| `tariff` | number |  |
| `type.color` | string |  |
| `type.id` | string |  |
| `type.label` | string |  |
| `type.tariff` | string |  |
| `type.type` | string |  |
| `type.vatclass.id` | string |  |
| `type.vatclass.label` | string |  |
| `type.vatclass.percentage` | number |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Simplicate API, this operation is `GET /hours/hours` (base URL `https://{{credentials.subdomain}}/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-hours.md) for the provider-specific parameters and requirements.

