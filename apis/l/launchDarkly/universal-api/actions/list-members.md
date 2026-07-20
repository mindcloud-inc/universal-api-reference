# LaunchDarkly: List Members

Retrieves account members from LaunchDarkly.

```
GET https://connect.mindcloud.co/v1/universal/launchDarkly/latest/actions/list-members
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LaunchDarkly `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/launchDarkly/latest/actions/list-members?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/launchDarkly/latest/actions/list-members?${params}`, {
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
      "creationDate": 1,
      "customRoles": [
        {}
      ],
      "email": "ava@example.com",
      "excludedDashboards": [
        "string"
      ],
      "firstName": "Ava",
      "id": "string",
      "isBeta": true,
      "lastName": "Chen",
      "lastSeen": 1,
      "links": {},
      "mfa": "string",
      "pendingInvite": true,
      "role": "string",
      "verified": true,
      "version": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `creationDate` | number |  |
| `customRoles` | array<object> |  |
| `email` | string |  |
| `excludedDashboards` | array<string> |  |
| `firstName` | string |  |
| `id` | string |  |
| `isBeta` | boolean |  |
| `lastName` | string |  |
| `lastSeen` | number |  |
| `links` | object |  |
| `mfa` | string |  |
| `pendingInvite` | boolean |  |
| `role` | string |  |
| `verified` | boolean |  |
| `version` | number |  |

## Native endpoint

Through the native LaunchDarkly API, this operation is `GET /members` (base URL `https://app.launchdarkly.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-members.md) for the provider-specific parameters and requirements.

