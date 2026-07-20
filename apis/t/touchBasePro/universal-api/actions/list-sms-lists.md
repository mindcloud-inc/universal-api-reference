# TouchBasePro: List SMS Lists

Retrieves SMS lists from TouchBasePro.

```
GET https://connect.mindcloud.co/v1/universal/touchBasePro/latest/actions/list-sms-lists
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TouchBasePro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/touchBasePro/latest/actions/list-sms-lists?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/touchBasePro/latest/actions/list-sms-lists?${params}`, {
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
      "page": 1,
      "pageSize": 1,
      "totalPages": 1,
      "totalRecordCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data[]` | array<object> |  |
| `data[].dateCreated` | date |  |
| `data[].id` | number |  |
| `data[].name` | string |  |
| `page` | number |  |
| `pageSize` | number |  |
| `totalPages` | number |  |
| `totalRecordCount` | number |  |

## Native endpoint

Through the native TouchBasePro API, this operation is `GET /sms/lists?page={page}&pageSize={pageSize}` (base URL `https://api.touchbasepro.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-sms-lists.md) for the provider-specific parameters and requirements.

