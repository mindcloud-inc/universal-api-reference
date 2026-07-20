# boomApp Connect: Retrieve Delivery Status Updates

Retrieves outbound delivery status updates from boomApp Connect.

```
GET https://connect.mindcloud.co/v1/universal/boomAppConnect/latest/actions/retrieve-delivery-status-updates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a boomApp Connect `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/boomAppConnect/latest/actions/retrieve-delivery-status-updates?connectionId=$CONNECTION_ID&drs_after=YYYY-MM-DD%20HH%3AMM%3ASS" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "drs_after": "YYYY-MM-DD HH:MM:SS"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/boomAppConnect/latest/actions/retrieve-delivery-status-updates?${params}`, {
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
| `drs_after` | string | yes | Required by the Boomerang API when retrieving delivery receipts. Use format YYYY-MM-DD HH:MM:SS. Example: `YYYY-MM-DD HH:MM:SS`. |
| `start_transaction_id` | number | no | Return delivery receipts from this transaction ID onward. |
| `ignore_previous` | boolean | no | Exclude previously retrieved delivery receipts. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "drs": {
        "campaignName": "Ava Chen",
        "customParameter": "string",
        "destination": "string",
        "status": "string",
        "statusDate": "string",
        "transactionId": "string",
        "uniqueId": "string"
      },
      "hasMore": true,
      "message": "string",
      "status": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `drs` | array<object> | Delivery receipt status updates. |
| `drs.campaignName` | string | Campaign name. |
| `drs.customParameter` | string | Custom reference value. |
| `drs.destination` | string | Destination number or address. |
| `drs.status` | string | Delivery status. |
| `drs.statusDate` | string | Status update date. |
| `drs.transactionId` | string | Outbound transaction ID. |
| `drs.uniqueId` | string | Unique message ID. |
| `hasMore` | boolean | Whether more pages are available. |
| `message` | string | Response message. |
| `status` | number | Response status code. |

## Native endpoint

Through the native boomApp Connect API, this operation is `GET /v1/get_all_new_drs` (base URL `https://direct-api.apps.boomcomms.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-delivery-status-updates.md) for the provider-specific parameters and requirements.

