# Time Doctor: List Tags

Retrieves tags from Time Doctor.

```
GET https://connect.mindcloud.co/v1/universal/timeDoctor/latest/actions/list-tags
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Time Doctor `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/timeDoctor/latest/actions/list-tags?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/timeDoctor/latest/actions/list-tags?${params}`, {
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
      "creatorId": "string",
      "deleted": true,
      "id": "string",
      "managedUsers": 1,
      "managedUsersOnReports": 1,
      "modifiedAt": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "readOnly": true,
      "special": "string",
      "users": 1,
      "usersOnReports": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `creatorId` | string |  |
| `deleted` | boolean |  |
| `id` | string |  |
| `managedUsers` | number |  |
| `managedUsersOnReports` | number |  |
| `modifiedAt` | date |  |
| `name` | string |  |
| `readOnly` | boolean |  |
| `special` | string |  |
| `users` | number |  |
| `usersOnReports` | number |  |

## Native endpoint

Through the native Time Doctor API, this operation is `GET /api/1.0/tags` (base URL `https://api2.timedoctor.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-tags.md) for the provider-specific parameters and requirements.

