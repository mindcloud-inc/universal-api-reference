# Campaign Monitor: List Unconfirmed Subscribers

Retrieves unconfirmed subscribers from a Campaign Monitor list.

```
GET https://connect.mindcloud.co/v1/universal/campaignMonitor/latest/actions/list-unconfirmed-subscribers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Campaign Monitor `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/campaignMonitor/latest/actions/list-unconfirmed-subscribers?connectionId=$CONNECTION_ID&listId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "listId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/campaignMonitor/latest/actions/list-unconfirmed-subscribers?${params}`, {
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
| `listId` | string | yes | Campaign Monitor list identifier. |

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
        {}
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
| `numberOfPages` | number | Total number of pages available. |
| `orderDirection` | string | Direction used to order the result set. |
| `pageNumber` | number | Current response page number. |
| `pageSize` | number | Number of records returned per page. |
| `recordsOnThisPage` | number | Number of subscriber records in the current page. |
| `results` | array<object> | Unconfirmed subscriber rows returned by Campaign Monitor. |
| `resultsOrderedBy` | string | Field used to order the result set. |
| `totalNumberOfRecords` | number | Total number of matching subscriber records. |

## Native endpoint

Through the native Campaign Monitor API, this operation is `GET /lists/:listId/unconfirmed.json` (base URL `https://api.createsend.com/api/v3.3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-unconfirmed-subscribers.md) for the provider-specific parameters and requirements.

