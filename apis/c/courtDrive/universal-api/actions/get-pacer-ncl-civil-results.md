# Court Drive: Get PACER NCL Civil Results



```
GET https://connect.mindcloud.co/v1/universal/courtDrive/latest/actions/get-pacer-ncl-civil-results
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Court Drive `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/courtDrive/latest/actions/get-pacer-ncl-civil-results?connectionId=$CONNECTION_ID&pageNo=string&searchId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "pageNo": "string",
  "searchId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/courtDrive/latest/actions/get-pacer-ncl-civil-results?${params}`, {
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
| `pageNo` | string | yes | Result page number to retrieve. |
| `searchId` | string | yes | National civil search identifier. |

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

Through the native Court Drive API, this operation is `GET /pacer/ncl/civil/{search_id}` (base URL `https://v1.courtapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-pacer-ncl-civil-results.md) for the provider-specific parameters and requirements.

