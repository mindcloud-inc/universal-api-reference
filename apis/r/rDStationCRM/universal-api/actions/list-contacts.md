# RD Station CRM: List Contacts

Retrieves contacts from RD Station CRM.

```
GET https://connect.mindcloud.co/v1/universal/rDStationCRM/latest/actions/list-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RD Station CRM `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rDStationCRM/latest/actions/list-contacts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rDStationCRM/latest/actions/list-contacts?${params}`, {
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
        [
          {}
        ]
      ],
      "links": {
        "first": "https://example.com",
        "last": "https://example.com",
        "self": "https://example.com"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data[]` | array<object> |  |
| `data[].contextOrigin` | string |  |
| `data[].createdAt` | string |  |
| `data[].customFields` | object |  |
| `data[].emails[]` | array<object> |  |
| `data[].emails[].email` | string |  |
| `data[].id` | string |  |
| `data[].legalBases[]` | array<string> |  |
| `data[].name` | string |  |
| `data[].phones[]` | array<object> |  |
| `data[].phones[].phone` | string |  |
| `data[].socialProfiles[]` | array<string> |  |
| `data[].updatedAt` | string |  |
| `links` | object |  |
| `links.first` | string |  |
| `links.last` | string |  |
| `links.self` | string |  |

## Native endpoint

Through the native RD Station CRM API, this operation is `GET /contacts` (base URL `https://api.rd.services/crm/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-contacts.md) for the provider-specific parameters and requirements.

