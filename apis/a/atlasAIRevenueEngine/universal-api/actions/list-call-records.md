# Atlas AI Revenue Engine: List Call Records



```
GET https://connect.mindcloud.co/v1/universal/atlasAIRevenueEngine/latest/actions/list-call-records
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Atlas AI Revenue Engine `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/atlasAIRevenueEngine/latest/actions/list-call-records?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/atlasAIRevenueEngine/latest/actions/list-call-records?${params}`, {
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
| `assistantId` | string | no | Filter by assistant ID. |
| `callType` | string | no | Filter by call type. |
| `campaignId` | string | no | Filter by campaign ID. |
| `campaignType` | string | no | Filter by campaign type. |
| `customerPhoneNumber` | string | no | Filter by customer phone number. |
| `endDate` | string | no | Filter by end date (date-time). |
| `startDate` | string | no | Filter by start date (date-time). |
| `successResult` | string | no | Filter by success result. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Atlas AI Revenue Engine API returns.

## Native endpoint

Through the native Atlas AI Revenue Engine API, this operation is `GET /call` (base URL `https://api.youratlas.com/v1/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-call-records.md) for the provider-specific parameters and requirements.

