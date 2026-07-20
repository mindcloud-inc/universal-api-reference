# ThingsBoard: Get Dashboard

Retrieves a dashboard with configuration from ThingsBoard.

```
GET https://connect.mindcloud.co/v1/universal/thingsBoard/latest/actions/get-dashboard
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ThingsBoard `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/thingsBoard/latest/actions/get-dashboard?connectionId=$CONNECTION_ID&dashboardId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "dashboardId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/thingsBoard/latest/actions/get-dashboard?${params}`, {
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
| `dashboardId` | string | yes | The ThingsBoard dashboard ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdTime": 1,
      "id": {
        "entityType": "string",
        "id": "string"
      },
      "image": "string",
      "mobileHide": true,
      "mobileOrder": 1,
      "name": "Ava Chen",
      "ownerId": {
        "id": "string"
      },
      "tenantId": {
        "id": "string"
      },
      "title": "string",
      "version": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdTime` | number |  |
| `id.entityType` | string |  |
| `id.id` | string |  |
| `image` | string |  |
| `mobileHide` | boolean |  |
| `mobileOrder` | number |  |
| `name` | string |  |
| `ownerId.id` | string |  |
| `tenantId.id` | string |  |
| `title` | string |  |
| `version` | number |  |

## Native endpoint

Through the native ThingsBoard API, this operation is `GET /dashboard/:dashboardId` (base URL `{{credentials.baseUrl}}/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-dashboard.md) for the provider-specific parameters and requirements.

