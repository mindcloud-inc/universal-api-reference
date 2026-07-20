# EbulkSMS: Get SMS Delivery Reports

Retrieves SMS delivery reports from EbulkSMS.

```
GET https://connect.mindcloud.co/v1/universal/ebulkSMS/latest/actions/get-sms-delivery-reports
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EbulkSMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ebulkSMS/latest/actions/get-sms-delivery-reports?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ebulkSMS/latest/actions/get-sms-delivery-reports?${params}`, {
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
| `uniqueId` | string | no | Optional message ID to fetch delivery status for a specific SMS. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native EbulkSMS API returns.

## Native endpoint

Through the native EbulkSMS API, this operation is `GET /getdlr.json` (base URL `https://api.ebulksms.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-sms-delivery-reports.md) for the provider-specific parameters and requirements.

