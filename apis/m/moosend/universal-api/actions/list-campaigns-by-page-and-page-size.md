# Moosend: List Campaigns By Page And Page Size

Retrieves campaigns from Moosend by page and page size.

```
GET https://connect.mindcloud.co/v1/universal/moosend/latest/actions/list-campaigns-by-page-and-page-size
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Moosend `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/moosend/latest/actions/list-campaigns-by-page-and-page-size?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/moosend/latest/actions/list-campaigns-by-page-and-page-size?${params}`, {
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
| `page` | number | no | The page number to display results for. Returns the first page if not specified. |
| `pageSize` | number | no | The maximum number of results per page. This must be a positive integer up to 1000 . Returns 10 results per page if not specified. If a value greater than 1000 is specified, it is treated as 1000 . |
| `sortBy` | string | no | The name of the campaign property to sort results by. Possible values: Name , Subject , Status , DeliveredOn , and CreatedOn (Default). |
| `sortMethod` | string | no | Specifies the method to sort results. Possible values: DESC for descending and ASC (Default) for ascending. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "abCampaignType": "string",
      "abHoursToTest": "string",
      "abWinner": "string",
      "abWinnerSelectionType": "string",
      "campaignSource": "string",
      "campaignType": "string",
      "confirmationTo": "string",
      "createdOn": "2026-05-07T12:00:00.000Z",
      "deliveredOn": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "isTransactional": true,
      "mailingLists": [
        {}
      ],
      "name": "Ava Chen",
      "recipientsCount": 1,
      "scheduledFor": "string",
      "scheduledForTimezone": "string",
      "siteName": "Ava Chen",
      "status": 1,
      "subject": "string",
      "totalBounces": 1,
      "totalComplaints": 1,
      "totalForwards": 1,
      "totalLinkClicks": 1,
      "totalOpens": 1,
      "totalSent": 1,
      "totalUnsubscribes": 1,
      "uniqueForwards": 1,
      "uniqueLinkClicks": 1,
      "uniqueOpens": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `abCampaignType` | string |  |
| `abHoursToTest` | string |  |
| `abWinner` | string |  |
| `abWinnerSelectionType` | string |  |
| `campaignSource` | string |  |
| `campaignType` | string |  |
| `confirmationTo` | string |  |
| `createdOn` | date |  |
| `deliveredOn` | date |  |
| `id` | string |  |
| `isTransactional` | boolean |  |
| `mailingLists` | array<object> |  |
| `name` | string |  |
| `recipientsCount` | number |  |
| `scheduledFor` | string |  |
| `scheduledForTimezone` | string |  |
| `siteName` | string |  |
| `status` | number |  |
| `subject` | string |  |
| `totalBounces` | number |  |
| `totalComplaints` | number |  |
| `totalForwards` | number |  |
| `totalLinkClicks` | number |  |
| `totalOpens` | number |  |
| `totalSent` | number |  |
| `totalUnsubscribes` | number |  |
| `uniqueForwards` | number |  |
| `uniqueLinkClicks` | number |  |
| `uniqueOpens` | number |  |

## Native endpoint

Through the native Moosend API, this operation is `GET /campaigns/{{Page}}/{{PageSize}}.json` (base URL `https://api.moosend.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-campaigns-by-page-and-page-size.md) for the provider-specific parameters and requirements.

