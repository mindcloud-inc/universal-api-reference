# Solace PubSub+: Get Resource Assignments

Retrieves resource assignments from Solace PubSub+.

```
GET https://connect.mindcloud.co/v1/universal/solacePubSub/latest/actions/get-resource-assignments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Solace PubSub+ `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/solacePubSub/latest/actions/get-resource-assignments?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/solacePubSub/latest/actions/get-resource-assignments?${params}`, {
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
      "resourceId": "string",
      "resourceType": {},
      "rrbacRoleId": "string",
      "userGroupId": "string",
      "userId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `resourceId` | string |  |
| `resourceType` | object |  |
| `rrbacRoleId` | string |  |
| `userGroupId` | string |  |
| `userId` | string |  |

## Native endpoint

Through the native Solace PubSub+ API, this operation is `GET /api/v2/platform/rrbac/resourceAssignments` (base URL `https://api.solace.cloud`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-resource-assignments.md) for the provider-specific parameters and requirements.

