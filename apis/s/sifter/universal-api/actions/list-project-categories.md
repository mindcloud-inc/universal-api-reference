# Sifter: List Project Categories

Retrieves categories for a project from Sifter.

```
GET https://connect.mindcloud.co/v1/universal/sifter/latest/actions/list-project-categories
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sifter `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sifter/latest/actions/list-project-categories?connectionId=$CONNECTION_ID&projectId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sifter/latest/actions/list-project-categories?${params}`, {
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
| `projectId` | number | yes | The Sifter project ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "apiIssuesUrl": "https://example.com",
      "issuesUrl": "https://example.com",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `apiIssuesUrl` | string |  |
| `issuesUrl` | string |  |
| `name` | string |  |

## Native endpoint

Through the native Sifter API, this operation is `GET /projects/:project_id/categories` (base URL `https://{{credentials.subdomain}}.sifterapp.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-project-categories.md) for the provider-specific parameters and requirements.

