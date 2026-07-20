# Scaleway: Delete SSH Key

Deletes an existing SSH key from Scaleway.

```
DELETE https://connect.mindcloud.co/v1/universal/scaleway/latest/actions/delete-ssh-key
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Scaleway `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/scaleway/latest/actions/delete-ssh-key?connectionId=$CONNECTION_ID&sshKeyId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "sshKeyId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scaleway/latest/actions/delete-ssh-key?${params}`, {
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

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Scaleway API returns.

## Native endpoint

Through the native Scaleway API, this operation is `DELETE /iam/v1alpha1/ssh-keys/:ssh_key_id` (base URL `https://api.scaleway.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-ssh-key.md) for the provider-specific parameters and requirements.

