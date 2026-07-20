# NextLead: List Sales Columns

Retrieves sales stage columns from NextLead.

```
GET https://connect.mindcloud.co/v1/universal/nextLead/latest/actions/list-sales-columns
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NextLead `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nextLead/latest/actions/list-sales-columns?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nextLead/latest/actions/list-sales-columns?${params}`, {
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
      "color": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "id": "string",
      "isLostStage": true,
      "isPipelineStage": true,
      "isTurnoverStage": true,
      "isWinStage": true,
      "name": "Ava Chen",
      "order": 1,
      "organizationId": "string",
      "requireContact": true,
      "requireStructure": true,
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `color` | string |  |
| `createdAt` | date |  |
| `description` | string |  |
| `id` | string |  |
| `isLostStage` | boolean |  |
| `isPipelineStage` | boolean |  |
| `isTurnoverStage` | boolean |  |
| `isWinStage` | boolean |  |
| `name` | string |  |
| `order` | number |  |
| `organizationId` | string |  |
| `requireContact` | boolean |  |
| `requireStructure` | boolean |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native NextLead API, this operation is `GET /api/v2/receive/sales/get-columns` (base URL `https://dashboard.nextlead.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-sales-columns.md) for the provider-specific parameters and requirements.

