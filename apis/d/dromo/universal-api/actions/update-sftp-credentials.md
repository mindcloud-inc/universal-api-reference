# Dromo: Update SFTP Credentials

Updates existing SFTP credentials in Dromo.

```
PUT https://connect.mindcloud.co/v1/universal/dromo/latest/actions/update-sftp-credentials
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dromo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/dromo/latest/actions/update-sftp-credentials" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "hostname": "Ava Chen",
  "port": 1,
  "user": "string",
  "auth_type": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dromo/latest/actions/update-sftp-credentials', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "hostname": "Ava Chen",
    "port": 1,
    "user": "string",
    "auth_type": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Path parameter id. |
| `hostname` | string | yes | Request body field hostname. |
| `port` | number | yes | Request body field port. |
| `user` | string | yes | Request body field user. |
| `auth_type` | string | yes | Request body field auth_type. |
| `password` | string | no | Request body field password. |
| `private_key` | string | no | Request body field private_key. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Dromo API returns.

## Native endpoint

Through the native Dromo API, this operation is `PUT /headless/sftp/credentials/:id/` (base URL `https://app.dromo.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-sftp-credentials.md) for the provider-specific parameters and requirements.

