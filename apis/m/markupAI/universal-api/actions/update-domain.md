# Markup AI: Update Domain

Updates an existing terminology domain in Markup AI.

```
PUT https://connect.mindcloud.co/v1/universal/markupAI/latest/actions/update-domain
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Markup AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/markupAI/latest/actions/update-domain" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "domainId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/markupAI/latest/actions/update-domain', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "domainId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `domainId` | string | yes | UUID of the terminology domain to update. |
| `name` | string | no | Updated domain name. |
| `description` | string | no | Updated domain description. |

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
| `created_at` | date |  |
| `created_by` | string |  |
| `description` | string |  |
| `id` | string |  |
| `name` | string |  |
| `term_set_count` | number |  |
| `updated_at` | date |  |
| `updated_by` | string |  |

## Native endpoint

Through the native Markup AI API, this operation is `PATCH /v1/terminology/domains/:domain_id` (base URL `https://api.markup.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-domain.md) for the provider-specific parameters and requirements.

