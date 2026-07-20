# SMSGatewayCenter SMS: Read Credit History



```
GET https://connect.mindcloud.co/v1/universal/sMSGatewayCenterSMS/latest/actions/read-credit-history
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SMSGatewayCenter SMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sMSGatewayCenterSMS/latest/actions/read-credit-history?connectionId=$CONNECTION_ID&fromDate=YYYY-MM-DD&toDate=YYYY-MM-DD" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "fromDate": "YYYY-MM-DD",
  "toDate": "YYYY-MM-DD"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sMSGatewayCenterSMS/latest/actions/read-credit-history?${params}`, {
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
| `fromDate` | string | yes | Start date for the credit-history window as a literal provider date string, for example 2026-04-01. Example: `YYYY-MM-DD`. |
| `toDate` | string | yes | End date for the credit-history window as a literal provider date string, for example 2026-04-03. Example: `YYYY-MM-DD`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "response": {
        "action": "string",
        "api": "string",
        "code": "string",
        "count": 1,
        "historyList": [
          [
            {}
          ]
        ],
        "msg": "string",
        "status": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `response.action` | string | Provider action name. |
| `response.api` | string | Provider API family. |
| `response.code` | string | Provider response code. |
| `response.count` | number | Returned history-row count. |
| `response.historyList[]` | array<object> | Credit-history rows. |
| `response.msg` | string | Provider message. |
| `response.status` | string | Provider status label. |

## Native endpoint

Through the native SMSGatewayCenter SMS API, this operation is `POST /SMSApi/account/readcredithistory` (base URL `https://unify.smsgateway.center`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/read-credit-history.md) for the provider-specific parameters and requirements.

