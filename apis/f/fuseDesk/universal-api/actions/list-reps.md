# FuseDesk: List Reps

Retrieves active and disabled reps from FuseDesk.

```
GET https://connect.mindcloud.co/v1/universal/fuseDesk/latest/actions/list-reps
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FuseDesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fuseDesk/latest/actions/list-reps?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fuseDesk/latest/actions/list-reps?${params}`, {
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
      "active": true,
      "avatarUrl": "https://example.com",
      "dateCreated": "2026-05-07T12:00:00.000Z",
      "dateLastLogin": "2026-05-07T12:00:00.000Z",
      "dateUpdated": "2026-05-07T12:00:00.000Z",
      "defaultDepartmentId": 1,
      "emailAddress": "ava@example.com",
      "firstName": "Ava",
      "isArchived": true,
      "lastName": "Chen",
      "repid": 1,
      "timeZone": "string",
      "userId": 1,
      "username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `avatarUrl` | string |  |
| `dateCreated` | date |  |
| `dateLastLogin` | date |  |
| `dateUpdated` | date |  |
| `defaultDepartmentId` | number |  |
| `emailAddress` | string |  |
| `firstName` | string |  |
| `isArchived` | boolean |  |
| `lastName` | string |  |
| `repid` | number |  |
| `timeZone` | string |  |
| `userId` | number |  |
| `username` | string |  |

## Native endpoint

Through the native FuseDesk API, this operation is `GET /api/v2/reps` (base URL `https://{{credentials.appName}}.fusedesk.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-reps.md) for the provider-specific parameters and requirements.

