# Kite Suite: Get Dashboard By Dashboard ID



```
GET https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/get-dashboard-by-dashboard-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kite Suite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/get-dashboard-by-dashboard-id?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/get-dashboard-by-dashboard-id?${params}`, {
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
| `id` | string | yes | dashboardID |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_id": "string",
      "createAt": "string",
      "layout": "string",
      "name": "Ava Chen",
      "owner": "string",
      "privacy": "string",
      "updatedAt": "string",
      "widgets": [
        "string"
      ],
      "workspace": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_id` | string | The auto-generated id of the dashboard |
| `createAt` | string | Creation time of dashboard |
| `layout` | string | Layout selected |
| `name` | string | Name of dashboard |
| `owner` | string | Owner of dashboard |
| `privacy` | string | Privacy of dashboard |
| `updatedAt` | string | Updated time of dashboard |
| `widgets` | array | Widgets of dashboard |
| `workspace` | string | Workspace of dashboard |

## Native endpoint

Through the native Kite Suite API, this operation is `GET /api/v1/dashboard/:id` (base URL `https://api.kitesuite.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-dashboard-by-dashboard-id.md) for the provider-specific parameters and requirements.

