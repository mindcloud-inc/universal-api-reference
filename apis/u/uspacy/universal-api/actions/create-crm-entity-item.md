# Uspacy: Create CRM Entity Item

Creates a new CRM entity item in Uspacy.

```
POST https://connect.mindcloud.co/v1/universal/uspacy/latest/actions/create-crm-entity-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Uspacy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/uspacy/latest/actions/create-crm-entity-item" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "entity": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/uspacy/latest/actions/create-crm-entity-item', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "entity": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `entity` | string | yes | The CRM entity key. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "converted": true,
      "created_at": 1,
      "created_by": 1,
      "crm_tasks": [
        {}
      ],
      "id": 1,
      "letters": [
        {}
      ],
      "owner": 1,
      "table_name": "Ava Chen",
      "title": "string",
      "updated_at": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `converted` | boolean |  |
| `created_at` | number |  |
| `created_by` | number |  |
| `crm_tasks` | array<object> |  |
| `id` | number |  |
| `letters` | array<object> |  |
| `owner` | number |  |
| `table_name` | string |  |
| `title` | string |  |
| `updated_at` | number |  |

## Native endpoint

Through the native Uspacy API, this operation is `POST /crm/v1/entities/:entity` (base URL `https://{{credentials.site}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-crm-entity-item.md) for the provider-specific parameters and requirements.

