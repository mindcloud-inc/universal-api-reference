# GitHub: List Repository Labels



```
GET https://connect.mindcloud.co/v1/universal/github/latest/actions/list-repository-labels
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GitHub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/github/latest/actions/list-repository-labels?connectionId=$CONNECTION_ID&owner=string&repo=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "owner": "string",
  "repo": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/github/latest/actions/list-repository-labels?${params}`, {
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
| `owner` | string | yes | The account owner of the repository. The name is not case sensitive. |
| `repo` | string | yes | The name of the repository without the .git extension. The name is not case sensitive. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `per_page` | number | no | The number of results per page (max 100). Default: `100`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "color": "string",
      "default": true,
      "description": "string",
      "id": 1,
      "name": "Ava Chen",
      "nodeId": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `color` | string |  |
| `default` | boolean |  |
| `description` | string |  |
| `id` | number |  |
| `name` | string |  |
| `nodeId` | string |  |
| `url` | string |  |

## Native endpoint

Through the native GitHub API, this operation is `GET /repos/:owner/:repo/labels` (base URL `https://api.github.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-repository-labels.md) for the provider-specific parameters and requirements.

