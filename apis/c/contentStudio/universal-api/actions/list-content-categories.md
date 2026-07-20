# ContentStudio: List Content Categories

Retrieves content categories for a workspace from ContentStudio.

```
GET https://connect.mindcloud.co/v1/universal/contentStudio/latest/actions/list-content-categories
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ContentStudio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/contentStudio/latest/actions/list-content-categories?connectionId=$CONNECTION_ID&workspace_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workspace_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/contentStudio/latest/actions/list-content-categories?${params}`, {
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
| `page` | number | no | Page number for pagination. |
| `per_page` | number | no | Number of items per page. |
| `search` | string | no | Search term. |
| `workspace_id` | string | yes | ContentStudio workspace ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accounts": [
        {}
      ],
      "color": "string",
      "colorCode": "string",
      "Id": "string",
      "name": "Ava Chen",
      "postsCount": 1,
      "slotsCount": 1,
      "state": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accounts` | array<object> |  |
| `color` | string |  |
| `colorCode` | string |  |
| `Id` | string |  |
| `name` | string |  |
| `postsCount` | number |  |
| `slotsCount` | number |  |
| `state` | string |  |

## Native endpoint

Through the native ContentStudio API, this operation is `GET /workspaces/:workspace_id/content-categories` (base URL `https://api.contentstudio.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-content-categories.md) for the provider-specific parameters and requirements.

