# Rocketlane: Remove Project Members

Removes members from a project in Rocketlane.

```
PUT https://connect.mindcloud.co/v1/universal/rocketlane/latest/actions/remove-project-members
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rocketlane `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/rocketlane/latest/actions/remove-project-members" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectId": 1,
  "members": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rocketlane/latest/actions/remove-project-members', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectId": 1,
    "members": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `projectId` | number | yes | The project's unique, system-generated identifier, which can be used to identify the project globally. |
| `members` | list<object> | yes | The team members from your organization working on the project. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archived": true,
      "createdAt": 1,
      "createdBy": {},
      "currency": "string",
      "customer": {},
      "dueDate": "string",
      "fields": [
        {}
      ],
      "financials": {},
      "owner": {},
      "partnerCompanies": [
        {}
      ],
      "projectId": 1,
      "projectName": "Ava Chen",
      "startDate": "string",
      "status": {},
      "teamMembers": {},
      "updatedAt": 1,
      "updatedBy": {},
      "visibility": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archived` | boolean | The field `archived` denotes whether the project is archived or not. If the project is archived, there's an option to un-archive the project. |
| `createdAt` | number | The time when the project was created. The referenced time will be in epoch millis. |
| `createdBy` | object | The team member who created the project. |
| `currency` | string | The currency for handling the project’s financials. You can only specify a currency for a project that is added at the account level. Please note that the project’s currency cannot to changed once set. |
| `customer` | object | Company details for the invoice |
| `dueDate` | string | The day on which the project's execution is planned to be completed. The due date is not required and can be left blank. If sources (templates) are included as part of the project creation, the project's due date will be calculated depending on the duration of the specified sources. For projects where both startDate and dueDate are specified, the latter must be on or after the given startDate. The format for the due date is _YYYY-MM-DD_. |
| `fields` | array<object> | Fields lists the custom project fields whose values were provided during project creation or updated later. Refer these [examples](https://developer.rocketlane.com/v1.0/docs/custom-fields#examples-of-requests-and-responses-for-assigning-custom-field-values) to know more about different types of custom fields returned in response. |
| `financials` | object | This section addresses the financial aspects of the projects and the associated fields. |
| `owner` | object | The project owner is the team member who has access to everything in the project and is in charge of managing it. Any team member can be assigned as the project owner during the project creation or can be modified later.  In the absence of a selection, the project owner is set to the team member who created the project by default. |
| `partnerCompanies` | array<object> | The `partners` field contains list of partner companies. |
| `projectId` | number | The project's unique, system-generated identifier, which can be used to identify the project globally. |
| `projectName` | string | The name of the project. |
| `startDate` | string | On this date the project's execution officially begins. If sources (templates) are mentioned in the request, the start date is required. For projects without any defined sources, it may be empty. The format for the start date is _YYYY-MM-DD_. |
| `status` | object | The project status value along with the label will be present here. |
| `teamMembers` | object | The teamMembers field can be used to specify the project members, customers and customerChampion. Once the project is created, an invite will be emailed to all the teamMembers specified. |
| `updatedAt` | number | The time when the project was updated. Any changes that's related to the project are captured and specified here in epoch millis. |
| `updatedBy` | object | The team member who updated the project |
| `visibility` | string | Set visibility parameters to restrict who can see your project. There are two options: `EVERYONE` and `MEMBERS`. Selecting `EVERYONE` allows all team members from your firm to view the project, while selecting `MEMBER` restricts access to only those team members who have been specifically invited. |

## Native endpoint

Through the native Rocketlane API, this operation is `POST /1.0/projects/:projectId/remove-members` (base URL `https://api.rocketlane.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-project-members.md) for the provider-specific parameters and requirements.

