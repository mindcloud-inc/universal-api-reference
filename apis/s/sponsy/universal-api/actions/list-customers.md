# Sponsy: List Customers

Retrieves customers from Sponsy.

```
GET https://connect.mindcloud.co/v1/universal/sponsy/latest/actions/list-customers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sponsy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sponsy/latest/actions/list-customers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sponsy/latest/actions/list-customers?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "allowPortalReports": true,
      "archivedAt": "2026-05-07T12:00:00.000Z",
      "contacts": [
        {}
      ],
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "includeInMetrics": true,
      "name": "Ava Chen",
      "portalId": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "workspaceId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `allowPortalReports` | boolean | Whether portal reporting is enabled. |
| `archivedAt` | date | Archive timestamp when present. |
| `contacts` | array<object> | Primary and additional customer contacts. |
| `createdAt` | date | Customer creation timestamp. |
| `id` | string | Sponsy customer ID. |
| `includeInMetrics` | boolean | Whether the customer is included in metrics. |
| `name` | string | Customer name. |
| `portalId` | string | Customer portal ID. |
| `updatedAt` | date | Customer update timestamp. |
| `workspaceId` | string | Workspace ID for the customer. |

## Native endpoint

Through the native Sponsy API, this operation is `GET /v1/customers` (base URL `https://api.getsponsy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-customers.md) for the provider-specific parameters and requirements.

