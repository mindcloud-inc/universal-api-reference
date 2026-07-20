# Zoho Sprints: List Workspace Users

Retrieves workspace users from Zoho Sprints.

```
GET https://connect.mindcloud.co/v1/universal/zohoSprints/latest/actions/list-workspace-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Sprints `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoSprints/latest/actions/list-workspace-users?connectionId=$CONNECTION_ID&teamId=string&index=1&range=100" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "teamId": "string",
  "index": "1",
  "range": "100"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoSprints/latest/actions/list-workspace-users?${params}`, {
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
| `teamId` | string | yes |  |
| `index` | number | yes | Default: `1`. |
| `range` | number | yes | Default: `100`. |
| `type` | number | no | Default: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "next": true,
      "status": "string",
      "user_prop": {},
      "userIds": [
        "string"
      ],
      "userJObj": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `next` | boolean |  |
| `status` | string |  |
| `user_prop` | object |  |
| `userIds` | array<string> |  |
| `userJObj` | object |  |

## Native endpoint

Through the native Zoho Sprints API, this operation is `GET /team/:teamId/users/` (base URL `https://sprintsapi.zoho.com/zsapi`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-workspace-users.md) for the provider-specific parameters and requirements.

