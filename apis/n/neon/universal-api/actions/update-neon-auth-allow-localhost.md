# Neon: Update allow localhost

Updates localhost allow setting in Neon.

```
PUT https://connect.mindcloud.co/v1/universal/neon/latest/actions/update-neon-auth-allow-localhost
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Neon `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/neon/latest/actions/update-neon-auth-allow-localhost" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "project_id": "string",
  "branch_id": "string",
  "allow_localhost": true
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/neon/latest/actions/update-neon-auth-allow-localhost', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "project_id": "string",
    "branch_id": "string",
    "allow_localhost": true
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `project_id` | string | yes | Neon API parameter project_id |
| `branch_id` | string | yes | Neon API parameter branch_id |
| `allow_localhost` | boolean | yes | Neon API parameter allow_localhost |

## Response

```json
{
  "success": true,
  "data": [
    {
      "allow_localhost": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `allow_localhost` | boolean |  |

## Native endpoint

Through the native Neon API, this operation is `PATCH /projects/:project_id/branches/:branch_id/auth/allow_localhost` (base URL `https://console.neon.tech/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-neon-auth-allow-localhost.md) for the provider-specific parameters and requirements.

