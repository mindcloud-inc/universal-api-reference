# Scaleway: Get SSH Key

Retrieves an SSH key from Scaleway.

```
GET https://connect.mindcloud.co/v1/universal/scaleway/latest/actions/get-ssh-key
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Scaleway `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scaleway/latest/actions/get-ssh-key?connectionId=$CONNECTION_ID&sshKeyId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "sshKeyId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scaleway/latest/actions/get-ssh-key?${params}`, {
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
| `sshKeyId` | string | yes |  |

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

Through the native Scaleway API, this operation is `GET /iam/v1alpha1/ssh-keys/:ssh_key_id` (base URL `https://api.scaleway.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-ssh-key.md) for the provider-specific parameters and requirements.

