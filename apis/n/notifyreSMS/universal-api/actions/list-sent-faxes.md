# Notifyre SMS: List Sent Faxes

Retrieves sent fax messages from Notifyre.

```
GET https://connect.mindcloud.co/v1/universal/notifyreSMS/latest/actions/list-sent-faxes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Notifyre SMS `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/notifyreSMS/latest/actions/list-sent-faxes?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/notifyreSMS/latest/actions/list-sent-faxes?${params}`, {
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
| `fromDate` | string | no | Inclusive start date filter for sent faxes. |
| `statusType` | string | no | Status filter for sent faxes. |
| `toDate` | string | no | Inclusive end date filter for sent faxes. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "faxes": [
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
| `faxes` | array<object> | Sent faxes matching the requested filters. |
| `total` | number | Total matching sent faxes. |

## Native endpoint

Through the native Notifyre SMS API, this operation is `GET /fax/send` (base URL `https://api.notifyre.com/20220711`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-sent-faxes.md) for the provider-specific parameters and requirements.

