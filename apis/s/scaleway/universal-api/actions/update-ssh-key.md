# Scaleway: Update SSH Key

Updates an existing SSH key in Scaleway.

```
PUT https://connect.mindcloud.co/v1/universal/scaleway/latest/actions/update-ssh-key
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Scaleway `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/scaleway/latest/actions/update-ssh-key" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "sshKeyId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/scaleway/latest/actions/update-ssh-key', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "sshKeyId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `sshKeyId` | string | yes |  |
| `name` | string | no |  |
| `disabled` | boolean | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "2026-05-07T12:00:00.000Z",
      "disabled": true,
      "fingerprint": "string",
      "id": "string",
      "name": "Ava Chen",
      "organization_id": "string",
      "project_id": "string",
      "public_key": "string",
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | date |  |
| `disabled` | boolean |  |
| `fingerprint` | string |  |
| `id` | string |  |
| `name` | string |  |
| `organization_id` | string |  |
| `project_id` | string |  |
| `public_key` | string |  |
| `updated_at` | date |  |

## Native endpoint

Through the native Scaleway API, this operation is `PATCH /iam/v1alpha1/ssh-keys/:ssh_key_id` (base URL `https://api.scaleway.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-ssh-key.md) for the provider-specific parameters and requirements.

