# Viqeo: Authenticate Project User

Authenticates a project user in Viqeo.

```
POST https://connect.mindcloud.co/v1/universal/viqeo/latest/actions/authenticate-project-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Viqeo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/viqeo/latest/actions/authenticate-project-user" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectId": "string",
  "email": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/viqeo/latest/actions/authenticate-project-user', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectId": "string",
    "email": "ava@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `projectId` | string | yes | Project identifier from the path. |
| `email` | string | yes | Project user email address. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "token": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `token` | string | Temporary token used to open the Viqeo Editor. |

## Native endpoint

Through the native Viqeo API, this operation is `POST /media-platform/v1/project/:projectId/user/:email/authenticate` (base URL `https://api.viqeo.tv`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/authenticate-project-user.md) for the provider-specific parameters and requirements.

