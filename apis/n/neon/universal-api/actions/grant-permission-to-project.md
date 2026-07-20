# Neon: Grant project access

Grants project access in Neon.

```
POST https://connect.mindcloud.co/v1/universal/neon/latest/actions/grant-permission-to-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Neon `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/neon/latest/actions/grant-permission-to-project" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "project_id": "string",
  "email": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/neon/latest/actions/grant-permission-to-project', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "project_id": "string",
    "email": "ava@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `project_id` | string | yes | Neon API parameter project_id |
| `email` | string | yes | Neon API parameter email |

## Response

```json
{
  "success": true,
  "data": [
    {
      "granted_at": "2026-05-07T12:00:00.000Z",
      "granted_to_email": "ava@example.com",
      "id": "string",
      "revoked_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `granted_at` | date |  |
| `granted_to_email` | string |  |
| `id` | string |  |
| `revoked_at` | date |  |

## Native endpoint

Through the native Neon API, this operation is `POST /projects/:project_id/permissions` (base URL `https://console.neon.tech/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/grant-permission-to-project.md) for the provider-specific parameters and requirements.

