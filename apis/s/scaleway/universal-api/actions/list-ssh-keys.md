# Scaleway: List SSH Keys

Retrieves SSH keys from Scaleway for a project.

```
GET https://connect.mindcloud.co/v1/universal/scaleway/latest/actions/list-ssh-keys
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Scaleway `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scaleway/latest/actions/list-ssh-keys?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scaleway/latest/actions/list-ssh-keys?${params}`, {
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
| `projectId` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ssh_keys": [
        {}
      ],
      "total_count": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ssh_keys` | array<object> |  |
| `total_count` | number |  |

## Native endpoint

Through the native Scaleway API, this operation is `GET /iam/v1alpha1/ssh-keys` (base URL `https://api.scaleway.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-ssh-keys.md) for the provider-specific parameters and requirements.

