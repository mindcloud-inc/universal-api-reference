# Priority: List AP Invoices

Retrieves AP invoices from Priority.

```
GET https://connect.mindcloud.co/v1/universal/priority/latest/actions/list-ap-invoices
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Priority `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/priority/latest/actions/list-ap-invoices?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/priority/latest/actions/list-ap-invoices?${params}`, {
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
      "DEBIT": "string",
      "IVDATE": "2026-05-07T12:00:00.000Z",
      "IVNUM": "string",
      "IVTYPE": "string",
      "SUPNAME": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `DEBIT` | string |  |
| `IVDATE` | date |  |
| `IVNUM` | string |  |
| `IVTYPE` | string |  |
| `SUPNAME` | string |  |

## Native endpoint

Through the native Priority API, this operation is `GET /PINVOICES` (base URL `https://t.eu.priority-connect.online/odata/Priority/tabbtd38.ini/usdemo`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-ap-invoices.md) for the provider-specific parameters and requirements.

