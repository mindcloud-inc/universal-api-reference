# TrainerCentral: List Academy Learners

Retrieves academy learners from TrainerCentral.

```
GET https://connect.mindcloud.co/v1/universal/trainerCentral/latest/actions/list-academy-learners
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TrainerCentral `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/trainerCentral/latest/actions/list-academy-learners?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/trainerCentral/latest/actions/list-academy-learners?${params}`, {
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
      "email": "ava@example.com",
      "id": "string",
      "links": {
        "enrolledCourses": "https://example.com",
        "enrolledSessions": "https://example.com"
      },
      "loginType": "string",
      "name": "Ava Chen",
      "noofLogin": "string",
      "orgId": "string",
      "orgMemberId": "string",
      "role": "string",
      "status": "string",
      "time": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `email` | string |  |
| `id` | string |  |
| `links.enrolledCourses` | string |  |
| `links.enrolledSessions` | string |  |
| `loginType` | string |  |
| `name` | string |  |
| `noofLogin` | string |  |
| `orgId` | string |  |
| `orgMemberId` | string |  |
| `role` | string |  |
| `status` | string |  |
| `time` | string |  |

## Native endpoint

Through the native TrainerCentral API, this operation is `GET /portalMembers.json` (base URL `{{credentials.academyUrl}}/api/v4/{{credentials.orgId}}`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-academy-learners.md) for the provider-specific parameters and requirements.

