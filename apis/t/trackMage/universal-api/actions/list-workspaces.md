# TrackMage: List Workspaces

Retrieves workspaces from your TrackMage account.

```
GET https://connect.mindcloud.co/v1/universal/trackMage/latest/actions/list-workspaces
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TrackMage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/trackMage/latest/actions/list-workspaces?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/trackMage/latest/actions/list-workspaces?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `page` | number | no | The collection page number Default: `1`. |
| `itemsPerPage` | number | no | The number of items per page Default: `30`. |

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

Through the native TrackMage API, this operation is `GET /workspaces` (base URL `https://api.trackmage.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-workspaces.md) for the provider-specific parameters and requirements.

