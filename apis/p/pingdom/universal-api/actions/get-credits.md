# Pingdom: Get Credits



```
GET https://connect.mindcloud.co/v1/universal/pingdom/latest/actions/get-credits
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pingdom `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pingdom/latest/actions/get-credits?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pingdom/latest/actions/get-credits?${params}`, {
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
      "autofillsms": true,
      "autofillsmsAmount": 1,
      "autofillsmsWhenLeft": 1,
      "availablealertingfullusers": 1,
      "availablechecks": 1,
      "availabledefaultchecks": 1,
      "availablerumsites": 1,
      "availablesms": 1,
      "availablesmstests": 1,
      "availabletransactionchecks": 1,
      "checklimit": 1,
      "defaultchecklimit": 1,
      "maxalertingfullusers": 1,
      "maxrumfilters": 1,
      "maxrumpageviews": 1,
      "maxSmsOverage": 1,
      "transactionchecklimit": 1,
      "useddefault": 1,
      "usedrumsites": 1,
      "usedtransaction": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `autofillsms` | boolean | Whether SMS auto-fill is enabled. |
| `autofillsmsAmount` | number | Number of SMS credits to purchase when auto-fill triggers. |
| `autofillsmsWhenLeft` | number | Remaining SMS threshold that triggers auto-fill. |
| `availablealertingfullusers` | number | Available full alerting user seats remaining. |
| `availablechecks` | number | Available uptime check slots for new checks. |
| `availabledefaultchecks` | number | Available default uptime check slots for new checks. |
| `availablerumsites` | number | Available real user monitoring site slots. |
| `availablesms` | number | Remaining SMS credits on the account. |
| `availablesmstests` | number | Remaining SMS provider tests on the account. |
| `availabletransactionchecks` | number | Available transaction check slots for new checks. |
| `checklimit` | number | Total number of uptime check slots on the account. |
| `defaultchecklimit` | number | Total number of default uptime check slots on the account. |
| `maxalertingfullusers` | number | Maximum number of full alerting users allowed. |
| `maxrumfilters` | number | Maximum number of RUM filters allowed. |
| `maxrumpageviews` | number | Maximum monthly RUM pageviews allowed. |
| `maxSmsOverage` | number | Maximum SMS overage allowed, when enabled. |
| `transactionchecklimit` | number | Total number of transaction check slots on the account. |
| `useddefault` | number | Number of default check slots currently used. |
| `usedrumsites` | number | Number of real user monitoring sites currently used. |
| `usedtransaction` | number | Number of transaction check slots currently used. |

## Native endpoint

Through the native Pingdom API, this operation is `GET /credits` (base URL `https://api.pingdom.com/api/3.1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-credits.md) for the provider-specific parameters and requirements.

