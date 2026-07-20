# vPlan: Get Project



```
GET https://connect.mindcloud.co/v1/universal/vPlan/latest/actions/get-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a vPlan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vPlan/latest/actions/get-project?connectionId=$CONNECTION_ID&id=c7319bf7-9bd4-473c-9705-170d170988c2" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "c7319bf7-9bd4-473c-9705-170d170988c2"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vPlan/latest/actions/get-project?${params}`, {
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
| `id` | string | yes | Project identifier. Default: `c7319bf7-9bd4-473c-9705-170d170988c2`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": "string",
      "created_at": "string",
      "description": "string",
      "external_ref": "string",
      "id": "string",
      "name": "Ava Chen",
      "transaction": "string",
      "updated_at": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | string | Project code. |
| `created_at` | string | Creation timestamp. |
| `description` | string | Project description. |
| `external_ref` | string | External reference. |
| `id` | string | Project identifier. |
| `name` | string | Project name. |
| `transaction` | string | Provider transaction value. |
| `updated_at` | string | Last update timestamp. |

## Native endpoint

Through the native vPlan API, this operation is `GET /project/[:id]` (base URL `https://api.vplan.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-project.md) for the provider-specific parameters and requirements.

