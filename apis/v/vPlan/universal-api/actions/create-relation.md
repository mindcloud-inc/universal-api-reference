# vPlan: Create Relation



```
POST https://connect.mindcloud.co/v1/universal/vPlan/latest/actions/create-relation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a vPlan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/vPlan/latest/actions/create-relation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/vPlan/latest/actions/create-relation', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "string",
      "description": "string",
      "email": "ava@example.com",
      "external_ref": "string",
      "fax": "string",
      "id": "string",
      "name": "Ava Chen",
      "note": "string",
      "phone": "string",
      "type": "string",
      "updated_at": "string",
      "website": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | string | Creation timestamp. |
| `description` | string | Relation description. |
| `email` | string | Email address. |
| `external_ref` | string | External reference. |
| `fax` | string | Fax number. |
| `id` | string | Relation identifier. |
| `name` | string | Relation name. |
| `note` | string | Relation note. |
| `phone` | string | Phone number. |
| `type` | string | Relation type. |
| `updated_at` | string | Last update timestamp. |
| `website` | string | Website URL. |

## Native endpoint

Through the native vPlan API, this operation is `POST /relation` (base URL `https://api.vplan.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-relation.md) for the provider-specific parameters and requirements.

