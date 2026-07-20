# Datadog: Create Dashboard

Creates a new dashboard in Datadog.

```
POST https://connect.mindcloud.co/v1/universal/datadog/latest/actions/create-dashboard
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Datadog `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/datadog/latest/actions/create-dashboard" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "title": "string",
  "layoutType": "string",
  "widgets[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/datadog/latest/actions/create-dashboard', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "title": "string",
    "layoutType": "string",
    "widgets[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `title` | string | yes | Title of the dashboard. |
| `layoutType` | string | yes | Layout type of the dashboard. |
| `widgets[]` | array<object> | yes | List of widgets to display on the dashboard. |
| `description` | string | no | Description of the dashboard. |
| `notifyList[]` | array<string> | no | Handles of users to notify when changes are made to this dashboard. |
| `reflowType` | string | no | Reflow type for ordered dashboards. |
| `restrictedRoles[]` | array<string> | no | Role identifiers that can edit this dashboard. |
| `tags[]` | array<string> | no | Team tags representing dashboard ownership. |
| `templateVariables[]` | array<object> | no | Template variables for this dashboard. |
| `templateVariablePresets[]` | array<object> | no | Saved views for this dashboard's template variables. |

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

Through the native Datadog API, this operation is `POST /api/v1/dashboard` (base URL `https://api.us5.datadoghq.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-dashboard.md) for the provider-specific parameters and requirements.

