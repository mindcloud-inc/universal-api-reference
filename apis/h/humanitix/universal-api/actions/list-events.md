# Humanitix: List Events

Retrieves events from Humanitix for the connected account.

```
GET https://connect.mindcloud.co/v1/universal/humanitix/latest/actions/list-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Humanitix `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/humanitix/latest/actions/list-events?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/humanitix/latest/actions/list-events?${params}`, {
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
      "events": [
        [
          {}
        ]
      ],
      "page": 1,
      "pageSize": 1,
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `events[]` | array<object> |  |
| `events[].additionalQuestions[]` | array<string> |  |
| `events[].affiliateCodes[]` | array<string> |  |
| `events[].classification` | object |  |
| `events[].classification.category` | string |  |
| `events[].classification.subcategory` | string |  |
| `events[].classification.type` | string |  |
| `events[].createdAt` | string |  |
| `events[].currency` | string |  |
| `events[].dates[]` | array<object> |  |
| `events[].dates[].deleted` | boolean |  |
| `events[].dates[].disabled` | boolean |  |
| `events[].dates[].endDate` | string |  |
| `events[].dates[].id` | string |  |
| `events[].dates[].startDate` | string |  |
| `events[].description` | string |  |
| `events[].endDate` | string |  |
| `events[].eventLocation` | object |  |
| `events[].eventLocation.addressComponents[]` | array<string> |  |
| `events[].eventLocation.latLng[]` | array<string> |  |
| `events[].eventLocation.type` | string |  |
| `events[].eventModules[]` | array<object> |  |
| `events[].eventModules[].children[]` | array<string> |  |
| `events[].eventModules[].component` | string |  |
| `events[].eventModules[].id` | string |  |
| `events[].eventModules[].isEventDescription` | boolean |  |
| `events[].eventModules[].moduleType` | string |  |
| `events[].eventModules[].props` | object |  |
| `events[].eventModules[].props.content` | string |  |
| `events[].eventModules[].props.title` | string |  |
| `events[].id` | string |  |
| `events[].keywords[]` | array<string> |  |
| `events[].location` | string |  |
| `events[].markedAsSoldOut` | boolean |  |
| `events[].name` | string |  |
| `events[].packagedTickets[]` | array<string> |  |
| `events[].paymentOptions` | object |  |
| `events[].paymentOptions.refundSettings` | object |  |
| `events[].paymentOptions.refundSettings.customRefundPolicy` | string |  |
| `events[].paymentOptions.refundSettings.refundPolicy` | string |  |
| `events[].pricing` | object |  |
| `events[].pricing.maximumPrice` | number |  |
| `events[].pricing.minimumPrice` | number |  |
| `events[].public` | boolean |  |
| `events[].published` | boolean |  |
| `events[].sharingDescription` | string |  |
| `events[].slug` | string |  |
| `events[].startDate` | string |  |
| `events[].suspendSales` | boolean |  |
| `events[].tagIds[]` | array<string> |  |
| `events[].ticketTypes[]` | array<object> |  |
| `events[].ticketTypes[].deleted` | boolean |  |
| `events[].ticketTypes[].disabled` | boolean |  |
| `events[].ticketTypes[].id` | string |  |
| `events[].ticketTypes[].isDonation` | boolean |  |
| `events[].ticketTypes[].name` | string |  |
| `events[].ticketTypes[].price` | number |  |
| `events[].ticketTypes[].quantity` | number |  |
| `events[].timezone` | string |  |
| `events[].totalCapacity` | number |  |
| `events[].updatedAt` | string |  |
| `events[].url` | string |  |
| `events[].userId` | string |  |
| `page` | number |  |
| `pageSize` | number |  |
| `total` | number |  |

## Native endpoint

Through the native Humanitix API, this operation is `GET /events` (base URL `https://api.humanitix.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-events.md) for the provider-specific parameters and requirements.

