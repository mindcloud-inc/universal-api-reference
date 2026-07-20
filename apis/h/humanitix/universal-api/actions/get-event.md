# Humanitix: Get Event

Retrieves an event from Humanitix by event ID.

```
GET https://connect.mindcloud.co/v1/universal/humanitix/latest/actions/get-event
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Humanitix `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/humanitix/latest/actions/get-event?connectionId=$CONNECTION_ID&eventId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "eventId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/humanitix/latest/actions/get-event?${params}`, {
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
| `eventId` | string | yes | The Humanitix event ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "additionalQuestions": [
        [
          "string"
        ]
      ],
      "affiliateCodes": [
        [
          "string"
        ]
      ],
      "classification": {
        "category": "string",
        "subcategory": "string",
        "type": "string"
      },
      "createdAt": "string",
      "currency": "string",
      "dates": [
        [
          {}
        ]
      ],
      "description": "string",
      "endDate": "string",
      "eventLocation": {
        "addressComponents": [
          [
            "string"
          ]
        ],
        "latLng": [
          [
            "string"
          ]
        ],
        "type": "string"
      },
      "eventModules": [
        [
          {}
        ]
      ],
      "id": "string",
      "keywords": [
        [
          "string"
        ]
      ],
      "location": "string",
      "markedAsSoldOut": true,
      "name": "Ava Chen",
      "packagedTickets": [
        [
          "string"
        ]
      ],
      "paymentOptions": {
        "refundSettings": {
          "customRefundPolicy": "string",
          "refundPolicy": "string"
        }
      },
      "pricing": {
        "maximumPrice": 1,
        "minimumPrice": 1
      },
      "public": true,
      "published": true,
      "sharingDescription": "string",
      "slug": "string",
      "startDate": "string",
      "suspendSales": true,
      "tagIds": [
        [
          "string"
        ]
      ],
      "ticketTypes": [
        [
          {}
        ]
      ],
      "timezone": "string",
      "totalCapacity": 1,
      "updatedAt": "string",
      "url": "https://example.com",
      "userId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `additionalQuestions[]` | array<string> |  |
| `affiliateCodes[]` | array<string> |  |
| `classification` | object |  |
| `classification.category` | string |  |
| `classification.subcategory` | string |  |
| `classification.type` | string |  |
| `createdAt` | string |  |
| `currency` | string |  |
| `dates[]` | array<object> |  |
| `dates[].deleted` | boolean |  |
| `dates[].disabled` | boolean |  |
| `dates[].endDate` | string |  |
| `dates[].id` | string |  |
| `dates[].startDate` | string |  |
| `description` | string |  |
| `endDate` | string |  |
| `eventLocation` | object |  |
| `eventLocation.addressComponents[]` | array<string> |  |
| `eventLocation.latLng[]` | array<string> |  |
| `eventLocation.type` | string |  |
| `eventModules[]` | array<object> |  |
| `eventModules[].children[]` | array<string> |  |
| `eventModules[].component` | string |  |
| `eventModules[].id` | string |  |
| `eventModules[].isEventDescription` | boolean |  |
| `eventModules[].moduleType` | string |  |
| `eventModules[].props` | object |  |
| `eventModules[].props.content` | string |  |
| `eventModules[].props.title` | string |  |
| `id` | string |  |
| `keywords[]` | array<string> |  |
| `location` | string |  |
| `markedAsSoldOut` | boolean |  |
| `name` | string |  |
| `packagedTickets[]` | array<string> |  |
| `paymentOptions` | object |  |
| `paymentOptions.refundSettings` | object |  |
| `paymentOptions.refundSettings.customRefundPolicy` | string |  |
| `paymentOptions.refundSettings.refundPolicy` | string |  |
| `pricing` | object |  |
| `pricing.maximumPrice` | number |  |
| `pricing.minimumPrice` | number |  |
| `public` | boolean |  |
| `published` | boolean |  |
| `sharingDescription` | string |  |
| `slug` | string |  |
| `startDate` | string |  |
| `suspendSales` | boolean |  |
| `tagIds[]` | array<string> |  |
| `ticketTypes[]` | array<object> |  |
| `ticketTypes[].deleted` | boolean |  |
| `ticketTypes[].disabled` | boolean |  |
| `ticketTypes[].id` | string |  |
| `ticketTypes[].isDonation` | boolean |  |
| `ticketTypes[].name` | string |  |
| `ticketTypes[].price` | number |  |
| `ticketTypes[].quantity` | number |  |
| `timezone` | string |  |
| `totalCapacity` | number |  |
| `updatedAt` | string |  |
| `url` | string |  |
| `userId` | string |  |

## Native endpoint

Through the native Humanitix API, this operation is `GET /events/:eventId` (base URL `https://api.humanitix.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-event.md) for the provider-specific parameters and requirements.

