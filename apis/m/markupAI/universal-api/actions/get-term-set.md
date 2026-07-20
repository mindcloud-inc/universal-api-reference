# Markup AI: Get Term Set

Retrieves term set details from Markup AI.

```
GET https://connect.mindcloud.co/v1/universal/markupAI/latest/actions/get-term-set
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Markup AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/markupAI/latest/actions/get-term-set?connectionId=$CONNECTION_ID&termSetId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "termSetId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/markupAI/latest/actions/get-term-set?${params}`, {
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
| `termSetId` | string | yes | UUID of the term set. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "2026-05-07T12:00:00.000Z",
      "created_by": "string",
      "domains": [
        {}
      ],
      "id": "string",
      "instructions": "string",
      "terms": [
        {}
      ],
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
| `domains` | array<object> |  |
| `id` | string |  |
| `instructions` | string |  |
| `terms` | array<object> |  |
| `updated_at` | date |  |
| `updated_by` | string |  |

## Native endpoint

Through the native Markup AI API, this operation is `GET /v1/terminology/term-sets/:term_set_id` (base URL `https://api.markup.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-term-set.md) for the provider-specific parameters and requirements.

