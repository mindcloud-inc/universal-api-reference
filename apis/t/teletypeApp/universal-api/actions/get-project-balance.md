# Teletype App: Get Project Balance

Retrieves project balance from Teletype App.

```
GET https://connect.mindcloud.co/v1/universal/teletypeApp/latest/actions/get-project-balance
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Teletype App `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/teletypeApp/latest/actions/get-project-balance?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/teletypeApp/latest/actions/get-project-balance?${params}`, {
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
      "balance": 1,
      "paidUntilDate": "2026-05-07T12:00:00.000Z",
      "promisedPayment": 1,
      "promoDaysRemain": 1,
      "promoEndDate": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `balance` | number |  |
| `paidUntilDate` | date |  |
| `promisedPayment` | number |  |
| `promoDaysRemain` | number |  |
| `promoEndDate` | date |  |

## Native endpoint

Through the native Teletype App API, this operation is `GET /project/balance` (base URL `https://api.teletype.app/public/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-project-balance.md) for the provider-specific parameters and requirements.

