# TouchBasePro: List Unconfirmed Subscribers in List

Retrieves unconfirmed subscribers in a list from TouchBasePro.

```
GET https://connect.mindcloud.co/v1/universal/touchBasePro/latest/actions/list-unconfirmed-subscribers-in-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TouchBasePro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/touchBasePro/latest/actions/list-unconfirmed-subscribers-in-list?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/touchBasePro/latest/actions/list-unconfirmed-subscribers-in-list?${params}`, {
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
      "numberOfPages": 1,
      "orderDirection": "string",
      "pageNumber": 1,
      "pageSize": 1,
      "recordsOnThisPage": 1,
      "results": [
        [
          {}
        ]
      ],
      "resultsOrderedBy": "string",
      "totalNumberOfRecords": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `numberOfPages` | number |  |
| `orderDirection` | string |  |
| `pageNumber` | number |  |
| `pageSize` | number |  |
| `recordsOnThisPage` | number |  |
| `results[]` | array<object> |  |
| `results[].customFields[]` | array<object> |  |
| `results[].customFields[].key` | string |  |
| `results[].customFields[].value` | string |  |
| `results[].date` | date |  |
| `results[].emailAddress` | string |  |
| `results[].name` | string |  |
| `results[].state` | string |  |
| `resultsOrderedBy` | string |  |
| `totalNumberOfRecords` | number |  |

## Native endpoint

Through the native TouchBasePro API, this operation is `GET /email/lists/{listId}/unconfirmed` (base URL `https://api.touchbasepro.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-unconfirmed-subscribers-in-list.md) for the provider-specific parameters and requirements.

