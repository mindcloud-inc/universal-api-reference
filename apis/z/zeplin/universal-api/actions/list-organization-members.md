# Zeplin: List Organization Members

Retrieves a list of organization members from Zeplin.

```
GET https://connect.mindcloud.co/v1/universal/zeplin/latest/actions/list-organization-members
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zeplin `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zeplin/latest/actions/list-organization-members?connectionId=$CONNECTION_ID&limit=25&offset=0&organizationId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "organizationId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zeplin/latest/actions/list-organization-members?${params}`, {
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
| `organizationId` | string | yes | Organization id |
| `handle[]` | array<string> | no | Filter organization members by email, username or unique identifier of the user ☝️Note that only organization admins (or higher) can filter members using email addresses. Example: `?handle=zozo&handle=5d9caaecb4a3fa9bc9718686&handle=zozo%40zeplin.io` |

## Response

```json
{
  "success": true,
  "data": [
    {
      "invited": 1,
      "restricted": true,
      "role": "string",
      "tags": [
        "string"
      ],
      "user": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `invited` | number |  |
| `restricted` | boolean |  |
| `role` | string |  |
| `tags` | array<string> |  |
| `user` | object |  |

## Native endpoint

Through the native Zeplin API, this operation is `GET /organizations/{organization_id}/members` (base URL `https://api.zeplin.dev/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-organization-members.md) for the provider-specific parameters and requirements.

