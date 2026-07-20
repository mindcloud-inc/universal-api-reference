# Court Drive: Search PACER NCL All Courts Cases



```
GET https://connect.mindcloud.co/v1/universal/courtDrive/latest/actions/search-pacer-ncl-all-courts-cases
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Court Drive `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/courtDrive/latest/actions/search-pacer-ncl-all-courts-cases?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/courtDrive/latest/actions/search-pacer-ncl-all-courts-cases?${params}`, {
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
      "cases": [
        {}
      ],
      "config": {},
      "links": {},
      "parties": [
        {}
      ],
      "receipts": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cases` | array<object> |  |
| `config` | object |  |
| `links` | object |  |
| `parties` | array<object> |  |
| `receipts` | array<object> |  |

## Native endpoint

Through the native Court Drive API, this operation is `POST /pacer/ncl/all` (base URL `https://v1.courtapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-pacer-ncl-all-courts-cases.md) for the provider-specific parameters and requirements.

