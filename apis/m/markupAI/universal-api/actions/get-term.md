# Markup AI: Get Term

Retrieves term details from Markup AI.

```
GET https://connect.mindcloud.co/v1/universal/markupAI/latest/actions/get-term
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Markup AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/markupAI/latest/actions/get-term?connectionId=$CONNECTION_ID&termSetId=string&termId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "termSetId": "string",
  "termId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/markupAI/latest/actions/get-term?${params}`, {
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
| `termSetId` | string | yes | UUID of the parent term set. |
| `termId` | string | yes | UUID of the term. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "2026-05-07T12:00:00.000Z",
      "created_by": "string",
      "id": "string",
      "term": "string",
      "type": "string",
      "updated_at": "2026-05-07T12:00:00.000Z",
      "updated_by": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | date |  |
| `created_by` | string |  |
| `id` | string |  |
| `term` | string |  |
| `type` | string |  |
| `updated_at` | date |  |
| `updated_by` | string |  |

## Native endpoint

Through the native Markup AI API, this operation is `GET /v1/terminology/term-sets/:term_set_id/terms/:term_id` (base URL `https://api.markup.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-term.md) for the provider-specific parameters and requirements.

