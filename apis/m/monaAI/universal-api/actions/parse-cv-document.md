# Mona AI: Parse CV Document

Parses a CV document in Mona AI.

```
GET https://connect.mindcloud.co/v1/universal/monaAI/latest/actions/parse-cv-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mona AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/monaAI/latest/actions/parse-cv-document?connectionId=$CONNECTION_ID&permission=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "permission": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/monaAI/latest/actions/parse-cv-document?${params}`, {
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
| `cvData` | string | no | Inline CV text or data to parse when no URL is used. |
| `cvUrl` | string | no | URL of the CV document to parse. |
| `parseOptions` | object | no | Parsing options object controlling extracted CV sections. |
| `permission` | string | yes | Mona permission string required by the CV parsing endpoint. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Mona AI API returns.

## Native endpoint

Through the native Mona AI API, this operation is `POST /parsing/parseCV` (base URL `https://api.mona-ai.cloud`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/parse-cv-document.md) for the provider-specific parameters and requirements.

