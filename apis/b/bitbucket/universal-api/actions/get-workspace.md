# Bitbucket: Get Workspace

Retrieves a workspace from Bitbucket.

```
GET https://connect.mindcloud.co/v1/universal/bitbucket/latest/actions/get-workspace
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bitbucket `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bitbucket/latest/actions/get-workspace?connectionId=$CONNECTION_ID&workspace=mindcloudbitbucket20260409" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workspace": "mindcloudbitbucket20260409"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bitbucket/latest/actions/get-workspace?${params}`, {
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
| `workspace` | string | yes | Workspace slug, for example mindcloudbitbucket20260409. Default: `mindcloudbitbucket20260409`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "is_private": true,
      "name": "Ava Chen",
      "slug": "string",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `is_private` | boolean |  |
| `name` | string |  |
| `slug` | string |  |
| `uuid` | string |  |

## Native endpoint

Through the native Bitbucket API, this operation is `GET /workspaces/:workspace` (base URL `https://api.bitbucket.org/2.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-workspace.md) for the provider-specific parameters and requirements.

