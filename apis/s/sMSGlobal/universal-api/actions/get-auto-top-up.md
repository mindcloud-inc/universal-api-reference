# SMSGlobal: Get Auto Top-up

Retrieves auto top-up settings for the SMSGlobal account.

```
GET https://connect.mindcloud.co/v1/universal/sMSGlobal/latest/actions/get-auto-top-up
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SMSGlobal `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sMSGlobal/latest/actions/get-auto-top-up?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sMSGlobal/latest/actions/get-auto-top-up?${params}`, {
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
      "balanceAmount": 1,
      "balanceThreshold": 1,
      "card": {
        "number": "string",
        "type": "string"
      },
      "disabled": true,
      "periodicAmount": 1,
      "periodicEndDate": "2026-05-07T12:00:00.000Z",
      "periodicFrequency": 1,
      "periodicStartDate": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `balanceAmount` | number | The auto top-up amount. |
| `balanceThreshold` | number | The auto top-up low balance threshold. |
| `card.number` | string | Masked credit card number. |
| `card.type` | string | Credit card type. |
| `disabled` | boolean | Whether auto top-up is disabled for the authenticated account. |
| `periodicAmount` | number | The periodic top-up amount. |
| `periodicEndDate` | date | The auto top-up end date. |
| `periodicFrequency` | number | The auto top-up periodic frequency. |
| `periodicStartDate` | date | The auto top-up start date. |

## Native endpoint

Through the native SMSGlobal API, this operation is `GET /v2/auto-topup` (base URL `https://api.smsglobal.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-auto-top-up.md) for the provider-specific parameters and requirements.

