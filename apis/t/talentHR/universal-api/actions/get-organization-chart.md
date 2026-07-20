# TalentHR: Get Organization Chart

Retrieves the organization chart from TalentHR.

```
GET https://connect.mindcloud.co/v1/universal/talentHR/latest/actions/get-organization-chart
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TalentHR `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/talentHR/latest/actions/get-organization-chart?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/talentHR/latest/actions/get-organization-chart?${params}`, {
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
      "activeCycle": 1,
      "email": "ava@example.com",
      "firstName": "Ava",
      "id": 1,
      "isFutureRehire": true,
      "isOwner": 1,
      "jobTitle": "string",
      "jobTitleId": 1,
      "lastName": "Chen",
      "photoUrl": "https://example.com",
      "reportsToEmployeeId": 1,
      "resizedPhotoUrl": "https://example.com",
      "userId": 1,
      "userRole": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `activeCycle` | number | Current active cycle identifier. |
| `email` | string | Employee email address. |
| `firstName` | string | Employee first name. |
| `id` | number | Employee record ID. |
| `isFutureRehire` | boolean | Whether the employee is marked as a future rehire. |
| `isOwner` | number | Whether the employee is the workspace owner. |
| `jobTitle` | string | Job title name. |
| `jobTitleId` | number | Job title ID. |
| `lastName` | string | Employee last name. |
| `photoUrl` | string | Employee photo URL. |
| `reportsToEmployeeId` | number | Manager employee ID when present. |
| `resizedPhotoUrl` | string | Resized employee photo URL. |
| `userId` | number | Related user ID. |
| `userRole` | object | Nested user role details. |

## Native endpoint

Through the native TalentHR API, this operation is `GET /organization-chart` (base URL `https://pubapi.talenthr.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-organization-chart.md) for the provider-specific parameters and requirements.

