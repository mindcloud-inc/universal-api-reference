# Ubidots: Export Dashboard Model



```
GET https://connect.mindcloud.co/v1/universal/ubidots/latest/actions/export-dashboard-model
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ubidots `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ubidots/latest/actions/export-dashboard-model?connectionId=$CONNECTION_ID&dashboardKey=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "dashboardKey": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ubidots/latest/actions/export-dashboard-model?${params}`, {
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
| `dashboardKey` | string | yes | The dashboard ID or key. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "dashboard": {},
      "id": "string",
      "label": "string",
      "name": "Ava Chen",
      "settings": {},
      "variables": [
        {}
      ],
      "widgets": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `dashboard` | object |  |
| `id` | string |  |
| `label` | string |  |
| `name` | string |  |
| `settings` | object |  |
| `variables` | array<object> |  |
| `widgets` | array<object> |  |

## Native endpoint

Through the native Ubidots API, this operation is `GET /dashboards/:dashboard_key/_/export_models` (base URL `https://industrial.api.ubidots.com/api/v2.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/export-dashboard-model.md) for the provider-specific parameters and requirements.

