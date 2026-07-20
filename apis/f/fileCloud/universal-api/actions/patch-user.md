# FileCloud: Patch User

Partially updates an existing user in FileCloud.

```
PUT https://connect.mindcloud.co/v1/universal/fileCloud/latest/actions/patch-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FileCloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/fileCloud/latest/actions/patch-user" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "Operations[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/fileCloud/latest/actions/patch-user', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "Operations[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | User ID. |
| `Operations[]` | array<object> | yes | Patch operations, for example [{"op":"replace","path":"displayName","value":"apps"}]. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "displayName": "Ava Chen",
      "emails": [
        {}
      ],
      "groups": [
        {}
      ],
      "id": "string",
      "meta": {},
      "schemas": [
        "string"
      ],
      "userName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `displayName` | string |  |
| `emails` | array<object> |  |
| `groups` | array<object> |  |
| `id` | string |  |
| `meta` | object |  |
| `schemas` | array<string> |  |
| `userName` | string |  |

## Native endpoint

Through the native FileCloud API, this operation is `PATCH /scim/Users/:id` (base URL `https://mindcloud.filecloudtrial.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/patch-user.md) for the provider-specific parameters and requirements.

