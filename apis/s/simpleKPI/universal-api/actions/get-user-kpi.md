# SimpleKPI: Get User KPI

Retrieves a KPI assigned to a SimpleKPI user.

```
GET https://connect.mindcloud.co/v1/universal/simpleKPI/latest/actions/get-user-kpi
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SimpleKPI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/simpleKPI/latest/actions/get-user-kpi?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/simpleKPI/latest/actions/get-user-kpi?${params}`, {
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
| `id` | number | no | The KPI ID assigned to the user. |
| `userId` | number | no | The user ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "string",
      "id": 1,
      "sort_order": 1,
      "updated_at": "string",
      "user_id": 1,
      "user_target": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | string |  |
| `id` | number |  |
| `sort_order` | number |  |
| `updated_at` | string |  |
| `user_id` | number |  |
| `user_target` | string |  |

## Native endpoint

Through the native SimpleKPI API, this operation is `GET users/:userId/kpis/:id` (base URL `https://{{credentials.subdomain}}.simplekpi.com/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user-kpi.md) for the provider-specific parameters and requirements.

