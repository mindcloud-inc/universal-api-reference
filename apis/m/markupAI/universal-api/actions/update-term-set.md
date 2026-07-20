# Markup AI: Update Term Set

Updates an existing term set in Markup AI.

```
PUT https://connect.mindcloud.co/v1/universal/markupAI/latest/actions/update-term-set
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Markup AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/markupAI/latest/actions/update-term-set" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "termSetId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/markupAI/latest/actions/update-term-set', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "termSetId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `termSetId` | string | yes | UUID of the term set to update. |
| `instructions` | string | no | Updated instructions for the term set. |
| `domainIds[]` | array<string> | no | Updated terminology domain IDs for the term set. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "2026-05-07T12:00:00.000Z",
      "created_by": "string",
      "id": "string",
      "instructions": "string",
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
| `instructions` | string |  |
| `updated_at` | date |  |
| `updated_by` | string |  |

## Native endpoint

Through the native Markup AI API, this operation is `PATCH /v1/terminology/term-sets/:term_set_id` (base URL `https://api.markup.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-term-set.md) for the provider-specific parameters and requirements.

