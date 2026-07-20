# Edoobox: Get Category Dashboard

Retrieves a category dashboard from Edoobox.

```
GET https://connect.mindcloud.co/v1/universal/edoobox/latest/actions/get-category-dashboard
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Edoobox `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/edoobox/latest/actions/get-category-dashboard?connectionId=$CONNECTION_ID&categoryId=category_89bc96e49be5_7511246288" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "categoryId": "category_89bc96e49be5_7511246288"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/edoobox/latest/actions/get-category-dashboard?${params}`, {
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
| `categoryId` | string | yes | The edoobox category ID. Default: `category_89bc96e49be5_7511246288`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "category": true,
      "categoryId": "string",
      "categoryStats": {
        "chartLine": {
          "bookings": {
            "created": {
              "columns": [
                {
                  "field": "string",
                  "type": "string"
                }
              ]
            },
            "started": {
              "columns": [
                {
                  "field": "string",
                  "type": "string"
                }
              ]
            },
            "waitingList": {
              "columns": [
                {
                  "field": "string",
                  "type": "string"
                }
              ]
            }
          },
          "vouchers": {
            "columns": [
              {
                "field": "string",
                "type": "string"
              }
            ]
          }
        },
        "countBooking": 1,
        "countOffer": 1
      },
      "promotions": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `category` | boolean |  |
| `categoryId` | string |  |
| `categoryStats.chartLine.bookings.created.columns[].field` | string |  |
| `categoryStats.chartLine.bookings.created.columns[].type` | string |  |
| `categoryStats.chartLine.bookings.started.columns[].field` | string |  |
| `categoryStats.chartLine.bookings.started.columns[].type` | string |  |
| `categoryStats.chartLine.bookings.waitingList.columns[].field` | string |  |
| `categoryStats.chartLine.bookings.waitingList.columns[].type` | string |  |
| `categoryStats.chartLine.vouchers.columns[].field` | string |  |
| `categoryStats.chartLine.vouchers.columns[].type` | string |  |
| `categoryStats.countBooking` | number |  |
| `categoryStats.countOffer` | number |  |
| `promotions` | boolean |  |

## Native endpoint

Through the native Edoobox API, this operation is `GET /category/:category_id/dashboard` (base URL `https://app2.edoobox.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-category-dashboard.md) for the provider-specific parameters and requirements.

