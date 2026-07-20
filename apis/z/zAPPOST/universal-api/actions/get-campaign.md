# ZAP POST: Get Campaign

Retrieves a specific campaign from ZAP POST.

```
GET https://connect.mindcloud.co/v1/universal/zAPPOST/latest/actions/get-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ZAP POST `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zAPPOST/latest/actions/get-campaign?connectionId=$CONNECTION_ID&campaignId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "campaignId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zAPPOST/latest/actions/get-campaign?${params}`, {
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
| `campaignId` | string | yes | The campaign UUID to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "description": "string",
      "fields": [
        {}
      ],
      "id": "string",
      "name": "Ava Chen",
      "paperStockId": "string",
      "paperStockName": "Ava Chen",
      "startDate": "2026-05-07T12:00:00.000Z",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string | Campaign description. |
| `fields` | array<object> | Campaign custom field definitions. |
| `id` | string | Campaign identifier. |
| `name` | string | Campaign name. |
| `paperStockId` | string | Paper stock identifier. |
| `paperStockName` | string | Paper stock label. |
| `startDate` | date | Campaign start date. |
| `status` | string | Campaign status label. |

## Native endpoint

Through the native ZAP POST API, this operation is `GET /api/v1/campaign/:campaignId` (base URL `https://api.zappost.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-campaign.md) for the provider-specific parameters and requirements.

