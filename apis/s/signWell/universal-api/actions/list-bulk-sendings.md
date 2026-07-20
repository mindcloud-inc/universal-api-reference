# SignWell: List Bulk Sendings

Lists bulk sends available in SignWell.

```
GET https://connect.mindcloud.co/v1/universal/signWell/latest/actions/list-bulk-sendings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SignWell `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/signWell/latest/actions/list-bulk-sendings?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/signWell/latest/actions/list-bulk-sendings?${params}`, {
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
| `userEmail` | string | no | Email address of the user that sent the Bulk Send. |
| `limit` | number | no | Number of documents to fetch. Defaults to 10, max is 50. |
| `page` | number | no | Page number for pagination. |
| `apiApplicationId` | string | no | Unique identifier for API Application settings to use. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "currentPage": 1,
      "nextPage": {},
      "previousPage": {},
      "totalCount": 1,
      "totalPages": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `currentPage` | number |  |
| `nextPage` | object |  |
| `previousPage` | object |  |
| `totalCount` | number |  |
| `totalPages` | number |  |

## Native endpoint

Through the native SignWell API, this operation is `GET /bulk_sends` (base URL `https://www.signwell.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-bulk-sendings.md) for the provider-specific parameters and requirements.

