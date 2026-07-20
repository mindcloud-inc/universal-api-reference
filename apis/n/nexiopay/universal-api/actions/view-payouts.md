# Nexiopay: View payouts



```
GET https://connect.mindcloud.co/v1/universal/nexiopay/latest/actions/view-payouts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nexiopay `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nexiopay/latest/actions/view-payouts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nexiopay/latest/actions/view-payouts?${params}`, {
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
      "amount": 1,
      "currency": "string",
      "dateCreated": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "payoutId": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | number | Payout amount. |
| `currency` | string | Payout currency. |
| `dateCreated` | date | Payout creation timestamp. |
| `id` | string | Payout ID. |
| `payoutId` | string | Nexio payout ID. |
| `status` | string | Payout status. |

## Native endpoint

Through the native Nexiopay API, this operation is `GET /payout/v3` (base URL `https://api.nexiopaysandbox.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/view-payouts.md) for the provider-specific parameters and requirements.

