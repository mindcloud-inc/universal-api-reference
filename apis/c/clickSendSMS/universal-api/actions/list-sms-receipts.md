# ClickSend SMS: List SMS Receipts

Retrieves SMS receipts from ClickSend SMS.

```
GET https://connect.mindcloud.co/v1/universal/clickSendSMS/latest/actions/list-sms-receipts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ClickSend SMS `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clickSendSMS/latest/actions/list-sms-receipts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clickSendSMS/latest/actions/list-sms-receipts?${params}`, {
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
| `dateFrom` | string | no | Lower bound date filter for receipts. |
| `dateTo` | string | no | Upper bound date filter for receipts. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "currentPage": 1,
      "from": 1,
      "lastPage": 1,
      "nextPageUrl": {},
      "perPage": 1,
      "prevPageUrl": {},
      "to": 1,
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `currentPage` | number |  |
| `from` | number |  |
| `lastPage` | number |  |
| `nextPageUrl` | object |  |
| `perPage` | number |  |
| `prevPageUrl` | object |  |
| `to` | number |  |
| `total` | number |  |

## Native endpoint

Through the native ClickSend SMS API, this operation is `GET /v3/sms/receipts` (base URL `https://rest.clicksend.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-sms-receipts.md) for the provider-specific parameters and requirements.

