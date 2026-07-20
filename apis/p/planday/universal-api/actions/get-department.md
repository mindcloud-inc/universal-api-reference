# Planday: Get Department

Retrieves an existing department from Planday.

```
GET https://connect.mindcloud.co/v1/universal/planday/latest/actions/get-department
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Planday `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/planday/latest/actions/get-department?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/planday/latest/actions/get-department?${params}`, {
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
| `id` | number | yes |  |
| `includeDeleted` | boolean | no |  |
| `managedEmployeesOnly` | boolean | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "name": "Ava Chen",
      "number": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |
| `name` | string |  |
| `number` | string |  |

## Native endpoint

Through the native Planday API, this operation is `GET /hr/v1.0/departments/:id` (base URL `https://openapi.planday.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-department.md) for the provider-specific parameters and requirements.

