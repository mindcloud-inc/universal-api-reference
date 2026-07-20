# TelTel: List Inbound SMS Reports

Retrieves inbound SMS reports from your TelTel account.

```
GET https://connect.mindcloud.co/v1/universal/telTel/latest/actions/list-inbound-sms-reports
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TelTel `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/telTel/latest/actions/list-inbound-sms-reports?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/telTel/latest/actions/list-inbound-sms-reports?${params}`, {
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
      "createdAt": "2026-05-07T12:00:00.000Z",
      "from": "string",
      "id": "string",
      "message": "string",
      "to": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `from` | string |  |
| `id` | string |  |
| `message` | string |  |
| `to` | string |  |

## Native endpoint

Through the native TelTel API, this operation is `GET /sms/inbox/reports` (base URL `https://api.teltel.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-inbound-sms-reports.md) for the provider-specific parameters and requirements.

