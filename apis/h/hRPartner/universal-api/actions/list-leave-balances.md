# HR Partner: List Leave Balances



```
GET https://connect.mindcloud.co/v1/universal/hRPartner/latest/actions/list-leave-balances
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HR Partner `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hRPartner/latest/actions/list-leave-balances?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hRPartner/latest/actions/list-leave-balances?${params}`, {
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
      "absenceReason": "string",
      "autoAccrual": true,
      "balance": 1,
      "carryover": 1,
      "employee": {},
      "entitlement": 1,
      "isExternal": true,
      "lastAccrualDoneAt": "2026-05-07T12:00:00.000Z",
      "nextResetAt": "2026-05-07T12:00:00.000Z",
      "periodicIncrement": 1,
      "units": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `absenceReason` | string |  |
| `autoAccrual` | boolean |  |
| `balance` | number |  |
| `carryover` | number |  |
| `employee` | object |  |
| `entitlement` | number |  |
| `isExternal` | boolean |  |
| `lastAccrualDoneAt` | date |  |
| `nextResetAt` | date |  |
| `periodicIncrement` | number |  |
| `units` | string |  |

## Native endpoint

Through the native HR Partner API, this operation is `GET /leave_balances` (base URL `https://api.hrpartner.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-leave-balances.md) for the provider-specific parameters and requirements.

