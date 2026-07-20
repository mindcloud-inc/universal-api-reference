# PBX Yeastar: Query Company Contact List

Retrieves a list of company contacts from PBX Yeastar.

```
GET https://connect.mindcloud.co/v1/universal/pBXYeastar/latest/actions/query-company-contact-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PBX Yeastar `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pBXYeastar/latest/actions/query-company-contact-list?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pBXYeastar/latest/actions/query-company-contact-list?${params}`, {
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
      "data": [
        {}
      ],
      "errcode": 1,
      "errmsg": "string",
      "total_number": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> | Company contact records. |
| `errcode` | number | Yeastar result code. 0 means success. |
| `errmsg` | string | Yeastar result message. |
| `total_number` | number | Total records available. |

## Native endpoint

Through the native PBX Yeastar API, this operation is `GET /company_contact/list` (base URL `{{credentials.baseUrl}}/openapi/v1.0`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/query-company-contact-list.md) for the provider-specific parameters and requirements.

