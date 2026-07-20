# SMS Manager by BulkSMS.com.au: Get Sample Automation Event Data



```
GET https://connect.mindcloud.co/v1/universal/sMSManagerByBulkSMScomau/latest/actions/get-sample-automation-event-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SMS Manager by BulkSMS.com.au `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sMSManagerByBulkSMScomau/latest/actions/get-sample-automation-event-data?connectionId=$CONNECTION_ID&eventType=dlr" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "eventType": "dlr"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sMSManagerByBulkSMScomau/latest/actions/get-sample-automation-event-data?${params}`, {
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
| `eventType` | string | yes | Automation event type to fetch sample data for. One of: `dlr`, `mms_mo`, `sms_mo`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native SMS Manager by BulkSMS.com.au API returns.

## Native endpoint

Through the native SMS Manager by BulkSMS.com.au API, this operation is `GET /automations/samples/:event_type` (base URL `https://smsmanager.com.au/v2/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-sample-automation-event-data.md) for the provider-specific parameters and requirements.

