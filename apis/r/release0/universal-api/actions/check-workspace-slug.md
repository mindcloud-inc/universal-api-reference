# Release0: Check Workspace Slug

Checks whether a workspace slug is available in Release0.

```
GET https://connect.mindcloud.co/v1/universal/release0/latest/actions/check-workspace-slug
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Release0 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/release0/latest/actions/check-workspace-slug?connectionId=$CONNECTION_ID&slug=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "slug": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/release0/latest/actions/check-workspace-slug?${params}`, {
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
| `slug` | string | yes | The workspace slug to check. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "exists": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `exists` | boolean |  |

## Native endpoint

Through the native Release0 API, this operation is `GET /v1/workspaces/:slug/exists` (base URL `https://release0.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/check-workspace-slug.md) for the provider-specific parameters and requirements.

