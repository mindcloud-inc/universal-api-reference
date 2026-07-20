# HelpDocs: Get Article Versions

Retrieves article versions from HelpDocs.

```
GET https://connect.mindcloud.co/v1/universal/helpDocs/latest/actions/get-article-versions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HelpDocs `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/helpDocs/latest/actions/get-article-versions?connectionId=$CONNECTION_ID&articleId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "articleId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/helpDocs/latest/actions/get-article-versions?${params}`, {
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
| `articleId` | string | yes | Article ID to fetch versions for. |
| `languageCode` | string | no | Language version to inspect. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native HelpDocs API returns.

## Native endpoint

Through the native HelpDocs API, this operation is `GET /article/:article_id/versions` (base URL `https://api.helpdocs.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-article-versions.md) for the provider-specific parameters and requirements.

