# ZAP POST: List Campaigns

Retrieves campaign list from ZAP POST.

```
GET https://connect.mindcloud.co/v1/universal/zAPPOST/latest/actions/list-campaigns
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ZAP POST `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zAPPOST/latest/actions/list-campaigns?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zAPPOST/latest/actions/list-campaigns?${params}`, {
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
      "archivedDate": "2026-05-07T12:00:00.000Z",
      "clientId": "string",
      "csvPath": "string",
      "description": "string",
      "duration": 1,
      "enabled": true,
      "id": "string",
      "name": "Ava Chen",
      "paperStockId": "string",
      "startDate": "2026-05-07T12:00:00.000Z",
      "status": "string",
      "zapLimit": 1,
      "zapsSent": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archivedDate` | date | Archive timestamp when present. |
| `clientId` | string | Owning client identifier. |
| `csvPath` | string | CSV path value returned by the API. |
| `description` | string | Campaign description. |
| `duration` | number | Configured campaign duration. |
| `enabled` | boolean | Whether the campaign is enabled. |
| `id` | string | Campaign identifier. |
| `name` | string | Campaign name. |
| `paperStockId` | string | Paper stock identifier. |
| `startDate` | date | Campaign start date. |
| `status` | string | Campaign status label. |
| `zapLimit` | number | Configured zap limit. |
| `zapsSent` | number | Number of zaps sent for the campaign. |

## Native endpoint

Through the native ZAP POST API, this operation is `GET /api/v1/campaigns` (base URL `https://api.zappost.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-campaigns.md) for the provider-specific parameters and requirements.

