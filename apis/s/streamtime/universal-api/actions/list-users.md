# Streamtime: List Users



```
GET https://connect.mindcloud.co/v1/universal/streamtime/latest/actions/list-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Streamtime `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/streamtime/latest/actions/list-users?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/streamtime/latest/actions/list-users?${params}`, {
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
      "billableRate": 1,
      "branchId": 1,
      "costRate": 1,
      "displayName": "Ava Chen",
      "email": "ava@example.com",
      "firstName": "Ava",
      "hoursWorkedFriday": 1,
      "hoursWorkedMonday": 1,
      "hoursWorkedSaturday": 1,
      "hoursWorkedSunday": 1,
      "hoursWorkedThursday": 1,
      "hoursWorkedTuesday": 1,
      "hoursWorkedWednesday": 1,
      "id": 1,
      "lastName": "Chen",
      "phoneNumber": "string",
      "roleId": 1,
      "userStatus": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `billableRate` | number | Billable rate |
| `branchId` | number | Branch ID |
| `costRate` | number | Internal cost rate |
| `displayName` | string | Display name |
| `email` | string | User email address |
| `firstName` | string | First name |
| `hoursWorkedFriday` | number | Hours worked Friday |
| `hoursWorkedMonday` | number | Hours worked Monday |
| `hoursWorkedSaturday` | number | Hours worked Saturday |
| `hoursWorkedSunday` | number | Hours worked Sunday |
| `hoursWorkedThursday` | number | Hours worked Thursday |
| `hoursWorkedTuesday` | number | Hours worked Tuesday |
| `hoursWorkedWednesday` | number | Hours worked Wednesday |
| `id` | number | User ID |
| `lastName` | string | Last name |
| `phoneNumber` | string | Primary phone number |
| `roleId` | number | Role ID |
| `userStatus` | object | Current user status |

## Native endpoint

Through the native Streamtime API, this operation is `GET /users` (base URL `https://api.streamtime.net/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-users.md) for the provider-specific parameters and requirements.

