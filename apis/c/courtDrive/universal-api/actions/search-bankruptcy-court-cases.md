# Court Drive: Search Bankruptcy Court Cases



```
GET https://connect.mindcloud.co/v1/universal/courtDrive/latest/actions/search-bankruptcy-court-cases
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Court Drive `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/courtDrive/latest/actions/search-bankruptcy-court-cases?connectionId=$CONNECTION_ID&courtCode=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "courtCode": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/courtDrive/latest/actions/search-bankruptcy-court-cases?${params}`, {
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
| `courtCode` | string | yes | PACER bankruptcy court code for the search. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cases": [
        {}
      ],
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
| `links` | object |  |
| `parties` | array<object> |  |
| `receipts` | array<object> |  |

## Native endpoint

Through the native Court Drive API, this operation is `POST /courts/pacer/{court_code}/cases/search/bankruptcy` (base URL `https://v1.courtapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-bankruptcy-court-cases.md) for the provider-specific parameters and requirements.

