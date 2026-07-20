# AI Textraction: Extract Data

Extracts user-defined entities from unstructured text with AI Textraction.

```
GET https://connect.mindcloud.co/v1/universal/aITextraction/latest/actions/extract-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AI Textraction `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/aITextraction/latest/actions/extract-data?connectionId=$CONNECTION_ID&text=string&entities=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "text": "string",
  "entities": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/aITextraction/latest/actions/extract-data?${params}`, {
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
| `text` | string | yes | The free-form text to extract data from. |
| `entities` | object<object> | yes | A JSON array of entity definitions. Each item should include var_name, type, and description. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native AI Textraction API returns.

## Native endpoint

Through the native AI Textraction API, this operation is `POST /textraction` (base URL `https://ai-textraction.p.rapidapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/extract-data.md) for the provider-specific parameters and requirements.

