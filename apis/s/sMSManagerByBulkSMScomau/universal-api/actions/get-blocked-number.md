# SMS Manager by BulkSMS.com.au: Get Blocked Number



```
GET https://connect.mindcloud.co/v1/universal/sMSManagerByBulkSMScomau/latest/actions/get-blocked-number
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SMS Manager by BulkSMS.com.au `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sMSManagerByBulkSMScomau/latest/actions/get-blocked-number?connectionId=$CONNECTION_ID&blockedNumberId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "blockedNumberId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sMSManagerByBulkSMScomau/latest/actions/get-blocked-number?${params}`, {
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
| `blockedNumberId` | string | yes | Blocked number ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native SMS Manager by BulkSMS.com.au API returns.

## Native endpoint

Through the native SMS Manager by BulkSMS.com.au API, this operation is `GET /blocked_numbers/:blocked_number_id` (base URL `https://smsmanager.com.au/v2/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-blocked-number.md) for the provider-specific parameters and requirements.

