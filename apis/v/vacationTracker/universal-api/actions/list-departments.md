# Vacation Tracker: List Departments



```
GET https://connect.mindcloud.co/v1/universal/vacationTracker/latest/actions/list-departments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vacation Tracker `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vacationTracker/latest/actions/list-departments?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vacationTracker/latest/actions/list-departments?${params}`, {
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
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "isDefault": true,
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date | Creation timestamp. |
| `id` | string | Department ID. |
| `isDefault` | boolean | Whether this is the default department. |
| `name` | string | Department name. |

## Native endpoint

Through the native Vacation Tracker API, this operation is `GET /departments` (base URL `https://api.vacationtracker.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-departments.md) for the provider-specific parameters and requirements.

