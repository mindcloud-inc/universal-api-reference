# Productlane: Get Doc Article

Retrieves a help center article from Productlane.

```
GET https://connect.mindcloud.co/v1/universal/productlane/latest/actions/get-doc-article
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Productlane `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/productlane/latest/actions/get-doc-article?connectionId=$CONNECTION_ID&workspaceId=ba9bf7e6-fc19-40d3-9174-275a63e5fa74&articleId=95697bff-03d3-4ca1-b079-a153436116ba" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workspaceId": "ba9bf7e6-fc19-40d3-9174-275a63e5fa74",
  "articleId": "95697bff-03d3-4ca1-b079-a153436116ba"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/productlane/latest/actions/get-doc-article?${params}`, {
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
| `workspaceId` | string | yes | Workspace ID for the published docs site. Example: `ba9bf7e6-fc19-40d3-9174-275a63e5fa74`. |
| `articleId` | string | yes | Doc article ID. Example: `95697bff-03d3-4ca1-b079-a153436116ba`. |
| `language` | string | no | Optional language override. Example: `en`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Productlane API returns.

## Native endpoint

Through the native Productlane API, this operation is `GET /docs/articles/{workspaceId}/{articleId}` (base URL `https://productlane.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-doc-article.md) for the provider-specific parameters and requirements.

