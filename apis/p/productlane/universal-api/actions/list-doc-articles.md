# Productlane: List Doc Articles

Retrieves help center articles from Productlane.

```
GET https://connect.mindcloud.co/v1/universal/productlane/latest/actions/list-doc-articles
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Productlane `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/productlane/latest/actions/list-doc-articles?connectionId=$CONNECTION_ID&limit=25&offset=0&workspaceId=ba9bf7e6-fc19-40d3-9174-275a63e5fa74" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "workspaceId": "ba9bf7e6-fc19-40d3-9174-275a63e5fa74"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/productlane/latest/actions/list-doc-articles?${params}`, {
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
| `workspaceId` | string | yes | Workspace ID to list published doc articles for. Example: `ba9bf7e6-fc19-40d3-9174-275a63e5fa74`. |
| `language` | string | no | Optional language filter. Example: `en`. |
| `groupId` | string | no | Optional docs group filter. Example: `a48ae618-61e4-4ec1-b23a-56ac476c95d5`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Productlane API returns.

## Native endpoint

Through the native Productlane API, this operation is `GET /docs/articles/{workspaceId}` (base URL `https://productlane.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-doc-articles.md) for the provider-specific parameters and requirements.

