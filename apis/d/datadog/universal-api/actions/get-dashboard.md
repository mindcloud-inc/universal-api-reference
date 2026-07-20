# Datadog: Get Dashboard

Retrieves a dashboard from Datadog.

```
GET https://connect.mindcloud.co/v1/universal/datadog/latest/actions/get-dashboard
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Datadog `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/datadog/latest/actions/get-dashboard?connectionId=$CONNECTION_ID&dashboardId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "dashboardId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/datadog/latest/actions/get-dashboard?${params}`, {
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
| `dashboardId` | string | yes | The ID of the dashboard. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "authorHandle": "string",
      "authorName": "Ava Chen",
      "createdAt": "string",
      "description": "string",
      "id": "string",
      "isReadOnly": true,
      "layoutType": "string",
      "modifiedAt": "string",
      "notifyList": [
        "string"
      ],
      "reflowType": "string",
      "restrictedRoles": [
        "string"
      ],
      "tags": [
        "string"
      ],
      "templateVariablePresets": [
        {}
      ],
      "templateVariables": [
        {}
      ],
      "title": "string",
      "url": "https://example.com",
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
| `authorHandle` | string | Identifier of the dashboard author. |
| `authorName` | string | Name of the dashboard author. |
| `createdAt` | string | Creation timestamp. |
| `description` | string | Description of the dashboard. |
| `id` | string | ID of the dashboard. |
| `isReadOnly` | boolean | Whether the dashboard is read-only. |
| `layoutType` | string | Layout type of the dashboard. |
| `modifiedAt` | string | Last modification timestamp. |
| `notifyList` | array<string> | Users notified on dashboard changes. |
| `reflowType` | string | Reflow type for ordered dashboards. |
| `restrictedRoles` | array<string> | Roles allowed to edit the dashboard. |
| `tags` | array<string> | Ownership tags associated with the dashboard. |
| `templateVariablePresets` | array<object> | Saved template variable presets. |
| `templateVariables` | array<object> | Template variables configured on the dashboard. |
| `title` | string | Title of the dashboard. |
| `url` | string | URL of the dashboard. |
| `widgets` | array<object> | Widgets displayed on the dashboard. |

## Native endpoint

Through the native Datadog API, this operation is `GET /api/v1/dashboard/:dashboard_id` (base URL `https://api.us5.datadoghq.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-dashboard.md) for the provider-specific parameters and requirements.

