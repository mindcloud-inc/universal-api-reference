# vPlan: Get Resource



```
GET https://connect.mindcloud.co/v1/universal/vPlan/latest/actions/get-resource
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a vPlan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vPlan/latest/actions/get-resource?connectionId=$CONNECTION_ID&id=98a21931-d7ef-48de-9839-10565d5b3aab" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "98a21931-d7ef-48de-9839-10565d5b3aab"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vPlan/latest/actions/get-resource?${params}`, {
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
| `id` | string | yes | Resource identifier. Default: `98a21931-d7ef-48de-9839-10565d5b3aab`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archived_at": "string",
      "avatar": "string",
      "color_hex": "string",
      "created_at": "string",
      "deleted_at": "string",
      "description": "string",
      "end_date": "string",
      "external_ref": "string",
      "id": "string",
      "integration_schedule": true,
      "name": "Ava Chen",
      "start_date": "string",
      "transaction": "string",
      "type": "string",
      "updated_at": "string",
      "workdays": {},
      "workdays_start_date": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archived_at` | string | Archive timestamp. |
| `avatar` | string | Avatar URL. |
| `color_hex` | string | Resource color. |
| `created_at` | string | Creation timestamp. |
| `deleted_at` | string | Deletion timestamp. |
| `description` | string | Resource description. |
| `end_date` | string | End date. |
| `external_ref` | string | External reference. |
| `id` | string | Resource identifier. |
| `integration_schedule` | boolean | Whether integration scheduling is enabled. |
| `name` | string | Resource name. |
| `start_date` | string | Start date. |
| `transaction` | string | Provider transaction value. |
| `type` | string | Resource type. |
| `updated_at` | string | Last update timestamp. |
| `workdays` | object | Configured workdays map. |
| `workdays_start_date` | string | Workday schedule start date. |

## Native endpoint

Through the native vPlan API, this operation is `GET /resource/[:id]` (base URL `https://api.vplan.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-resource.md) for the provider-specific parameters and requirements.

