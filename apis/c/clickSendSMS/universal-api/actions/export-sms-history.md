# ClickSend SMS: Export SMS History

Exports SMS history from ClickSend SMS.

```
GET https://connect.mindcloud.co/v1/universal/clickSendSMS/latest/actions/export-sms-history
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ClickSend SMS `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clickSendSMS/latest/actions/export-sms-history?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clickSendSMS/latest/actions/export-sms-history?${params}`, {
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
| `filename` | string | no |  |
| `page` | number | no |  |
| `limit` | number | no |  |
| `q` | string | no |  |
| `order_by` | string | no |  |
| `date_from` | number | no |  |
| `date_to` | number | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `url` | string |  |

## Native endpoint

Through the native ClickSend SMS API, this operation is `GET /v3/sms/history/export` (base URL `https://rest.clicksend.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/export-sms-history.md) for the provider-specific parameters and requirements.

