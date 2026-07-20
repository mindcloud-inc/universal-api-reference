# Loopy Loyalty: List Events For Campaign



```
GET https://connect.mindcloud.co/v1/universal/loopyLoyalty/latest/actions/list-events-for-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Loopy Loyalty `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/loopyLoyalty/latest/actions/list-events-for-campaign?connectionId=$CONNECTION_ID&cid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "cid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/loopyLoyalty/latest/actions/list-events-for-campaign?${params}`, {
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
| `cid` | string | yes | Campaign ID. |
| `dt.start` | string | no | Initial paging row start number, 0 based. |
| `dt.length` | string | no | Number of rows to return. |
| `dt.search` | string | no | Search term applied to username. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `dt.order.column` | string | no | Column to sort by. |
| `dt.order.dir` | string | no | Sort direction. |
| `count` | boolean | no | Indicates if a count is returned or a list of records. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "campaignId": "string",
      "cardId": "string",
      "eventType": 1,
      "id": "string",
      "quantity": 1,
      "timestamp": "string",
      "username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `campaignId` | string | Campaign ID. |
| `cardId` | string | Card ID. |
| `eventType` | number | Event type code. |
| `id` | string | Event ID. |
| `quantity` | number | Event quantity. |
| `timestamp` | string | Event timestamp. |
| `username` | string | Username the event belongs to. |

## Native endpoint

Through the native Loopy Loyalty API, this operation is `POST /events/analytics/transactions/:cid` (base URL `https://api.loopyloyalty.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-events-for-campaign.md) for the provider-specific parameters and requirements.

