# Notifyre SMS: List SMS Replies

Retrieves received SMS replies from Notifyre.

```
GET https://connect.mindcloud.co/v1/universal/notifyreSMS/latest/actions/list-sms-replies
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Notifyre SMS `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/notifyreSMS/latest/actions/list-sms-replies?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/notifyreSMS/latest/actions/list-sms-replies?${params}`, {
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
| `fromDate` | string | no | Inclusive start date filter for SMS replies. |
| `toDate` | string | no | Inclusive end date filter for SMS replies. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "smsReplies": [
        {}
      ],
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `smsReplies` | array<object> | Received SMS replies matching the requested filters. |
| `total` | number | Total matching SMS replies. |

## Native endpoint

Through the native Notifyre SMS API, this operation is `GET /sms/received` (base URL `https://api.notifyre.com/20220711`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-sms-replies.md) for the provider-specific parameters and requirements.

