# TouchBasePro: List Campaign Clicks

Retrieves campaign click details from TouchBasePro.

```
GET https://connect.mindcloud.co/v1/universal/touchBasePro/latest/actions/list-campaign-clicks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TouchBasePro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/touchBasePro/latest/actions/list-campaign-clicks?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/touchBasePro/latest/actions/list-campaign-clicks?${params}`, {
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
| `results[].city` | string |  |
| `results[].countryCode` | string |  |
| `results[].countryName` | string |  |
| `results[].date` | date |  |
| `results[].emailAddress` | string |  |
| `results[].ipAddress` | string |  |
| `results[].latitude` | number |  |
| `results[].listId` | string |  |
| `results[].longitude` | number |  |
| `results[].region` | string |  |
| `results[].url` | string |  |
| `resultsOrderedBy` | string |  |
| `totalNumberOfRecords` | number |  |

## Native endpoint

Through the native TouchBasePro API, this operation is `GET /email/campaigns/{campaignId}/clicks` (base URL `https://api.touchbasepro.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-campaign-clicks.md) for the provider-specific parameters and requirements.

