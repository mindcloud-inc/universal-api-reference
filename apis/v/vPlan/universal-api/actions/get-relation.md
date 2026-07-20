# vPlan: Get Relation



```
GET https://connect.mindcloud.co/v1/universal/vPlan/latest/actions/get-relation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a vPlan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vPlan/latest/actions/get-relation?connectionId=$CONNECTION_ID&id=b7a5e9a6-dc09-441d-91f3-ab748f2747bc" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "b7a5e9a6-dc09-441d-91f3-ab748f2747bc"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vPlan/latest/actions/get-relation?${params}`, {
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
| `id` | string | yes | Relation identifier. Default: `b7a5e9a6-dc09-441d-91f3-ab748f2747bc`. |

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

Through the native vPlan API, this operation is `GET /relation/[:id]` (base URL `https://api.vplan.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-relation.md) for the provider-specific parameters and requirements.

