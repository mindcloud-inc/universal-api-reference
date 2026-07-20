# Vacation Tracker: List Users



```
GET https://connect.mindcloud.co/v1/universal/vacationTracker/latest/actions/list-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vacation Tracker `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vacationTracker/latest/actions/list-users?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vacationTracker/latest/actions/list-users?${params}`, {
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
| `status` | list<string> | no | Filter users by status. Defaults to ACTIVE. One of: `ACTIVE`, `DELETED`, `INACTIVE`. Default: `ACTIVE`. Example: `ACTIVE`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `locations` | string | no | Comma-separated list of location IDs to filter users. Accepts multiple values in one string, delimited by `,`. Example: `location-id-1,location-id-2`. |
| `departments` | string | no | Comma-separated list of department IDs to filter users. Accepts multiple values in one string, delimited by `,`. Example: `department-id-1,department-id-2`. |
| `labels` | string | no | Comma-separated list of labels to filter users. Accepts multiple values in one string, delimited by `,`. Example: `contractor,remote`. |
| `expand` | list<string> | no | Related user object to expand. One of: `department`, `holidays`, `location`. Example: `location`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "department": {
        "createdAt": "2026-05-07T12:00:00.000Z",
        "id": "string",
        "isDefault": true,
        "name": "Ava Chen"
      },
      "departmentId": "string",
      "email": "ava@example.com",
      "employeeId": "string",
      "endDate": "2026-05-07T12:00:00.000Z",
      "holidays": [
        {}
      ],
      "id": "string",
      "isAdmin": true,
      "labels": [
        "string"
      ],
      "location": {
        "createdAt": "2026-05-07T12:00:00.000Z",
        "id": "string",
        "isDefault": true,
        "name": "Ava Chen",
        "timezone": "string"
      },
      "locationId": "string",
      "name": "Ava Chen",
      "startDate": "2026-05-07T12:00:00.000Z",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `department.createdAt` | date | Expanded department creation timestamp. |
| `department.id` | string | Expanded department ID. |
| `department.isDefault` | boolean | Whether the expanded department is default. |
| `department.name` | string | Expanded department name. |
| `departmentId` | string | User department ID. |
| `email` | string | User email address. |
| `employeeId` | string | Employee ID when set. |
| `endDate` | date | Employment end timestamp when set. |
| `holidays` | array<object> | Expanded public holidays grouped by year when requested. |
| `id` | string | User ID. |
| `isAdmin` | boolean | Whether the user is an admin. |
| `labels` | array<string> | User labels. |
| `location.createdAt` | date | Expanded location creation timestamp. |
| `location.id` | string | Expanded location ID. |
| `location.isDefault` | boolean | Whether the expanded location is default. |
| `location.name` | string | Expanded location name. |
| `location.timezone` | string | Expanded location timezone. |
| `locationId` | string | User location ID. |
| `name` | string | User name. |
| `startDate` | date | Employment start timestamp. |
| `status` | string | User status. |

## Native endpoint

Through the native Vacation Tracker API, this operation is `GET /users` (base URL `https://api.vacationtracker.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-users.md) for the provider-specific parameters and requirements.

