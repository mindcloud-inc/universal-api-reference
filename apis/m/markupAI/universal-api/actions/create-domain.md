# Markup AI: Create Domain

Creates a new terminology domain in Markup AI.

```
POST https://connect.mindcloud.co/v1/universal/markupAI/latest/actions/create-domain
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Markup AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/markupAI/latest/actions/create-domain" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/markupAI/latest/actions/create-domain', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Name of the terminology domain. |
| `description` | string | no | Optional description for the terminology domain. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "2026-05-07T12:00:00.000Z",
      "created_by": "string",
      "description": "string",
      "id": "string",
      "name": "Ava Chen",
      "term_set_count": 1,
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
| `created_at` | date | UTC date and time when the domain was created. |
| `created_by` | string | Identifier of the actor that created the domain. |
| `description` | string | Optional description of the terminology domain. |
| `id` | string | Unique identifier of the terminology domain. |
| `name` | string | Name of the terminology domain. |
| `term_set_count` | number | Number of term sets associated with the domain. |
| `updated_at` | date | UTC date and time when the domain was last updated. |
| `updated_by` | string | Identifier of the actor that last updated the domain. |

## Native endpoint

Through the native Markup AI API, this operation is `POST /v1/terminology/domains` (base URL `https://api.markup.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-domain.md) for the provider-specific parameters and requirements.

