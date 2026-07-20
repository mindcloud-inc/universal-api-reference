# Bitbucket: Get Workspace Member

Retrieves a workspace member from Bitbucket.

```
GET https://connect.mindcloud.co/v1/universal/bitbucket/latest/actions/get-workspace-member
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bitbucket `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bitbucket/latest/actions/get-workspace-member?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bitbucket/latest/actions/get-workspace-member?${params}`, {
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
| `member` | string | no | Workspace member identifier. |
| `workspace` | string | no | Workspace slug. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "user": {},
      "workspace": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `user` | object |  |
| `workspace` | object |  |

## Native endpoint

Through the native Bitbucket API, this operation is `GET /workspaces/:workspace/members/:member` (base URL `https://api.bitbucket.org/2.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-workspace-member.md) for the provider-specific parameters and requirements.

