# Scaleway: Create SSH Key

Creates a new SSH key in Scaleway.

```
POST https://connect.mindcloud.co/v1/universal/scaleway/latest/actions/create-ssh-key
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Scaleway `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/scaleway/latest/actions/create-ssh-key" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "publicKey": "string",
  "projectId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/scaleway/latest/actions/create-ssh-key', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "publicKey": "string",
    "projectId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes |  |
| `publicKey` | string | yes |  |
| `projectId` | string | yes |  |

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

Through the native Scaleway API, this operation is `POST /iam/v1alpha1/ssh-keys` (base URL `https://api.scaleway.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-ssh-key.md) for the provider-specific parameters and requirements.

