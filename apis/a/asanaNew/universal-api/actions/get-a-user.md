# Asana: Get a user

Retrieves a user from Asana.

```
GET https://connect.mindcloud.co/v1/universal/asanaNew/latest/actions/get-a-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Asana `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/asanaNew/latest/actions/get-a-user?connectionId=$CONNECTION_ID&userGid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "userGid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/asanaNew/latest/actions/get-a-user?${params}`, {
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
| `optFields[]` | array<string> | no |  |
| `userGid` | string | yes | Path parameter: user_gid |

## Response

```json
{
  "success": true,
  "data": [
    {
      "email": "ava@example.com",
      "gid": "string",
      "name": "Ava Chen",
      "photo": {},
      "resourceType": "string",
      "workspaces": [
        {
          "gid": "string",
          "name": "Ava Chen",
          "resourceType": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `email` | string |  |
| `gid` | string |  |
| `name` | string |  |
| `photo` | object |  |
| `resourceType` | string |  |
| `workspaces[].gid` | string |  |
| `workspaces[].name` | string |  |
| `workspaces[].resourceType` | string |  |

## Native endpoint

Through the native Asana API, this operation is `GET users/:user_gid` (base URL `https://app.asana.com/api/1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-a-user.md) for the provider-specific parameters and requirements.

