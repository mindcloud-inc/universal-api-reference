# ClickSend SMS: List Numbers

Retrieves dedicated numbers from ClickSend SMS.

```
GET https://connect.mindcloud.co/v1/universal/clickSendSMS/latest/actions/list-numbers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ClickSend SMS `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clickSendSMS/latest/actions/list-numbers?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clickSendSMS/latest/actions/list-numbers?${params}`, {
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
| `page` | number | no | Page number. |
| `limit` | number | no | Items per page. |
| `q` | string | no | Search term for number records. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `exclude10dlcCampaign` | boolean | no | Exclude 10DLC campaign details from response. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "currency": {},
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
| `currency` | object |  |
| `currentPage` | number |  |
| `from` | number |  |
| `lastPage` | number |  |
| `nextPageUrl` | object |  |
| `perPage` | number |  |
| `prevPageUrl` | object |  |
| `to` | number |  |
| `total` | number |  |

## Native endpoint

Through the native ClickSend SMS API, this operation is `GET /v3/numbers` (base URL `https://rest.clicksend.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-numbers.md) for the provider-specific parameters and requirements.

