# DirectIQ: List Segment Contacts

Retrieves contacts matching segment criteria in DirectIQ.

```
GET https://connect.mindcloud.co/v1/universal/directiq/latest/actions/list-segment-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DirectIQ `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/directiq/latest/actions/list-segment-contacts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/directiq/latest/actions/list-segment-contacts?${params}`, {
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
      "columns": [
        [
          {}
        ]
      ],
      "hasNextPage": true,
      "maxStaticColumn": 1,
      "pageCount": 1,
      "pageNumber": 1,
      "pageSize": 1,
      "rows": [
        [
          {}
        ]
      ],
      "totalCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `columns[]` | array<object> |  |
| `columns[].displayName` | string |  |
| `columns[].isExtra` | boolean |  |
| `columns[].keyId` | number |  |
| `columns[].name` | string |  |
| `columns[].position` | number |  |
| `columns[].type` | number |  |
| `hasNextPage` | boolean |  |
| `maxStaticColumn` | number |  |
| `pageCount` | number |  |
| `pageNumber` | number |  |
| `pageSize` | number |  |
| `rows[]` | array<object> |  |
| `rows[].cells[]` | array<object> |  |
| `rows[].cells[].position` | number |  |
| `rows[].cells[].shouldLocalize` | boolean |  |
| `rows[].cells[].value` | string |  |
| `totalCount` | number |  |

## Native endpoint

Through the native DirectIQ API, this operation is `POST /contacts/segment/getcontacts` (base URL `https://rest.directiq.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-segment-contacts.md) for the provider-specific parameters and requirements.

