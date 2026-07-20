# Invision Community: Get CMS Category



```
GET https://connect.mindcloud.co/v1/universal/invisionCommunity/latest/actions/get-cms-category
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Invision Community `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/invisionCommunity/latest/actions/get-cms-category?connectionId=$CONNECTION_ID&database_id=1&category_id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "database_id": "1",
  "category_id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/invisionCommunity/latest/actions/get-cms-category?${params}`, {
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
| `database_id` | number | yes | Database identifier. |
| `category_id` | number | yes | Category identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "class": "string",
      "club": 1,
      "id": 1,
      "name": "Ava Chen",
      "parentId": 1,
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `class` | string |  |
| `club` | number |  |
| `id` | number |  |
| `name` | string |  |
| `parentId` | number |  |
| `url` | string |  |

## Native endpoint

Through the native Invision Community API, this operation is `GET /cms/databases/:database_id/:category_id` (base URL `{{credentials.communityBaseUrl}}/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-cms-category.md) for the provider-specific parameters and requirements.

