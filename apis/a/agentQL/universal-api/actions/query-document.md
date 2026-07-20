# AgentQL: Query Document

Queries structured data from documents and images with AgentQL.

```
GET https://connect.mindcloud.co/v1/universal/agentQL/latest/actions/query-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AgentQL `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/agentQL/latest/actions/query-document?connectionId=$CONNECTION_ID&file=string&body=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "file": "string",
  "body": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/agentQL/latest/actions/query-document?${params}`, {
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
| `file` | file | yes |  |
| `body` | string | yes | Stringified JSON containing query or prompt plus optional params. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native AgentQL API returns.

## Native endpoint

Through the native AgentQL API, this operation is `POST /v1/query-document` (base URL `https://api.agentql.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/query-document.md) for the provider-specific parameters and requirements.

