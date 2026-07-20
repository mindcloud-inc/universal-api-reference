# Trackabi: Get Project

Retrieves a project from Trackabi.

```
GET https://connect.mindcloud.co/v1/universal/trackabi/latest/actions/get-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Trackabi `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/trackabi/latest/actions/get-project?connectionId=$CONNECTION_ID&projectId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/trackabi/latest/actions/get-project?${params}`, {
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
| `projectId` | number | yes | The unique ID of the project. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assignedMembers": [
        {
          "address": "string",
          "avatar": "string",
          "birthdate": "string",
          "education": "string",
          "email": "ava@example.com",
          "emergencyContact": "string",
          "emergencyPhone": "string",
          "firstName": "Ava",
          "id": 1,
          "lastName": "Chen",
          "notes": "string",
          "personalEmail": "ava@example.com",
          "phone": "string"
        }
      ],
      "client": {
        "address": "string",
        "contactPerson": "string",
        "costHourlyRate": 1,
        "currency": "string",
        "email": "ava@example.com",
        "hourlyRate": 1,
        "id": 1,
        "logo": "string",
        "name": "Ava Chen",
        "notes": "string",
        "phone": "string",
        "shortName": "Ava Chen"
      },
      "costHourlyRate": "https://example.com",
      "currency": "string",
      "description": "string",
      "endDate": "string",
      "estimateUnits": "string",
      "hourlyRate": 1,
      "id": 1,
      "name": "Ava Chen",
      "notBillable": 1,
      "shortName": "Ava Chen",
      "startDate": "string",
      "teams": [
        {
          "id": 1,
          "name": "Ava Chen"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assignedMembers[].address` | string |  |
| `assignedMembers[].avatar` | string |  |
| `assignedMembers[].birthdate` | string |  |
| `assignedMembers[].education` | string |  |
| `assignedMembers[].email` | string |  |
| `assignedMembers[].emergencyContact` | string |  |
| `assignedMembers[].emergencyPhone` | string |  |
| `assignedMembers[].firstName` | string |  |
| `assignedMembers[].id` | number |  |
| `assignedMembers[].lastName` | string |  |
| `assignedMembers[].notes` | string |  |
| `assignedMembers[].personalEmail` | string |  |
| `assignedMembers[].phone` | string |  |
| `client.address` | string |  |
| `client.contactPerson` | string |  |
| `client.costHourlyRate` | number |  |
| `client.currency` | string |  |
| `client.email` | string |  |
| `client.hourlyRate` | number |  |
| `client.id` | number |  |
| `client.logo` | string |  |
| `client.name` | string |  |
| `client.notes` | string |  |
| `client.phone` | string |  |
| `client.shortName` | string |  |
| `costHourlyRate` | string |  |
| `currency` | string |  |
| `description` | string |  |
| `endDate` | string |  |
| `estimateUnits` | string |  |
| `hourlyRate` | number |  |
| `id` | number |  |
| `name` | string |  |
| `notBillable` | number |  |
| `shortName` | string |  |
| `startDate` | string |  |
| `teams[].id` | number |  |
| `teams[].name` | string |  |

## Native endpoint

Through the native Trackabi API, this operation is `GET /api/v1/projects/:projectId` (base URL `https://api.trackabi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-project.md) for the provider-specific parameters and requirements.

