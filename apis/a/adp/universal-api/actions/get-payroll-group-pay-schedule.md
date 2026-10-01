# ADP: Get Payroll Group Pay Schedule



```
GET https://connect.mindcloud.co/v1/universal/adp/latest/actions/get-payroll-group-pay-schedule
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ADP `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/adp/latest/actions/get-payroll-group-pay-schedule?connectionId=$CONNECTION_ID&groupCode=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "groupCode": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/adp/latest/actions/get-payroll-group-pay-schedule?${params}`, {
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
| `groupCode` | string | yes | The payroll group code whose pay schedule and pay periods should be returned. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native ADP API returns.

## Native endpoint

Through the native ADP API, this operation is `GET payroll/v1/pay-schedule/payroll-groups/:groupCode` (base URL `https://api.adp.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-payroll-group-pay-schedule.md) for the provider-specific parameters and requirements.

