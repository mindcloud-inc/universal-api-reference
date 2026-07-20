# TrackMage: Update Workspace

Updates an existing workspace in TrackMage.

```
PUT https://connect.mindcloud.co/v1/universal/trackMage/latest/actions/update-workspace
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TrackMage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/trackMage/latest/actions/update-workspace" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "title": "string",
  "defaultTrackingPage": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/trackMage/latest/actions/update-workspace', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "title": "string",
    "defaultTrackingPage": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Resource identifier |
| `title` | string | yes |  |
| `defaultTrackingPage` | object | yes |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `preferredCarriers[]` | array<string> | no |  |
| `considerShipmentDelayed` | object | no |  |
| `workflowsOrder[]` | array<string> | no |  |
| `logo` | string | no |  |
| `emailSettings.logo` | string | no |  |
| `emailSettings.signature` | string | no |  |
| `emailSettings.smtpCredentials` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "considerShipmentDelayed": {},
      "defaultTrackingPage": "string",
      "ecommerceIntegrationType": "string",
      "emailSettings": {},
      "id": "string",
      "logo": {
        "filePath": "string",
        "id": "string",
        "thumbnailPath": "string"
      },
      "members": [
        "string"
      ],
      "ordersCount": 1,
      "preferredCarriers": [
        "string"
      ],
      "scheduledForDelete": true,
      "shipmentsCount": 1,
      "team": "string",
      "title": "string",
      "widgets": [
        "string"
      ],
      "workflowsCount": 1,
      "workflowsOrder": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `considerShipmentDelayed` | object |  |
| `defaultTrackingPage` | string |  |
| `ecommerceIntegrationType` | string |  |
| `emailSettings` | object |  |
| `id` | string |  |
| `logo` | object |  |
| `logo.filePath` | string |  |
| `logo.id` | string |  |
| `logo.thumbnailPath` | string |  |
| `members` | array<string> |  |
| `ordersCount` | number |  |
| `preferredCarriers` | array<string> |  |
| `scheduledForDelete` | boolean |  |
| `shipmentsCount` | number |  |
| `team` | string |  |
| `title` | string |  |
| `widgets` | array<string> |  |
| `workflowsCount` | number |  |
| `workflowsOrder` | array<string> |  |

## Native endpoint

Through the native TrackMage API, this operation is `PUT /workspaces/{id}` (base URL `https://api.trackmage.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-workspace.md) for the provider-specific parameters and requirements.

