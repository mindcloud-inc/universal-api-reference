# Walmart: List Feed Statuses

Returns the feed statuses for all the specified Feed IDs.

```
GET https://connect.mindcloud.co/v1/universal/walmart/latest/actions/list-feed-statuses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Walmart `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/walmart/latest/actions/list-feed-statuses?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/walmart/latest/actions/list-feed-statuses?${params}`, {
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
| `feedId` | string | no | Unique ID returned by a bulk request. Used to track a Feed file. |
| `feedType` | list<string> | no | Define a type of feed to retrieve. #### Market Availability Feed types are specific to each market. These examples are not an exhaustive list. - *__Global__*: `MP_MAINTENANCE`, `MP_ITEM_MATCH`, `LAGTIME` - *__US, CA, MX__*: `MP_INVENTORY`, `SKU_TEMPLATE_MAP` - *__CA, MX, CL__*: `MP_ITEM_INTL` - *__US Only__*: `MP_ITEM`, `MP_WFS_ITEM`, `WALMART_FUNDED_INCENTIVES_ENROLLMENT`, `INCENTIVE_ENROLLMENT`, `PRICE_AND_PROMOTION`, `OMNI_WFS`, `RETIRE_ITEM`, `SHIPPING_OVERRIDES`, `FITMENT_ACES`, `FITMENT_PIES`, `SPLIT_AND_MERGE` - *__CA, MX__*: `OMNI_WFSSETUP`, `OMNI_WFSCONVERT` |
| `feedStatus` | list<string> | no | Status of the feed. Allowed: - RECEIVED - INPROGRESS - PROCESSED - ERROR |

## Response

```json
{
  "success": true,
  "data": [
    {
      "channelType": "string",
      "feedDate": 1,
      "feedId": "string",
      "feedSource": "string",
      "feedStatus": "string",
      "feedType": "string",
      "fileName": "Ava Chen",
      "itemDataErrorCount": 1,
      "itemsFailed": 1,
      "itemsProcessing": 1,
      "itemsReceived": 1,
      "itemsSucceeded": 1,
      "itemSystemErrorCount": 1,
      "itemTimeoutErrorCount": 1,
      "modifiedDtm": 1,
      "orgId": "string",
      "partnerId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `channelType` | string |  |
| `feedDate` | number |  |
| `feedId` | string |  |
| `feedSource` | string |  |
| `feedStatus` | string |  |
| `feedType` | string |  |
| `fileName` | string |  |
| `itemDataErrorCount` | number |  |
| `itemsFailed` | number |  |
| `itemsProcessing` | number |  |
| `itemsReceived` | number |  |
| `itemsSucceeded` | number |  |
| `itemSystemErrorCount` | number |  |
| `itemTimeoutErrorCount` | number |  |
| `modifiedDtm` | number |  |
| `orgId` | string |  |
| `partnerId` | string |  |

## Native endpoint

Through the native Walmart API, this operation is `GET /v3/feeds` (base URL `https://{{credentials.environment}}.walmartapis.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-feed-statuses.md) for the provider-specific parameters and requirements.

