# HirePOS: Create Website Booking

Creates a new website booking in HirePOS.

```
POST https://connect.mindcloud.co/v1/universal/hirePOS/latest/actions/create-website-booking
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HirePOS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/hirePOS/latest/actions/create-website-booking" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hirePOS/latest/actions/create-website-booking', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `addressLine1` | string | no | Primary booking address line. |
| `addressLine2` | string | no | Secondary booking address line. |
| `bookingDate` | date | no | Booking date for the website booking. |
| `city` | string | no | Booking city. |
| `comments` | string | no | Internal booking comments. |
| `company` | string | no | Booking company name. |
| `country` | string | no | Booking country. |
| `customField1` | string | no | Custom website booking field 1. |
| `customField2` | string | no | Custom website booking field 2. |
| `customField3` | string | no | Custom website booking field 3. |
| `customField4` | string | no | Custom website booking field 4. |
| `customField5` | string | no | Custom website booking field 5. |
| `customField6` | string | no | Custom website booking field 6. |
| `customField7` | string | no | Custom website booking field 7. |
| `customField8` | string | no | Custom website booking field 8. |
| `deliveryAddressLine1` | string | no | Primary delivery address line. |
| `deliveryAddressLine2` | string | no | Secondary delivery address line. |
| `deliveryCity` | string | no | Delivery city. |
| `deliveryPostcode` | string | no | Delivery postcode. |
| `deliveryState` | string | no | Delivery state. |
| `email` | string | no | Booking email address. |
| `estDateFrom` | date | no | Estimated booking start date and time. |
| `estDateTo` | date | no | Estimated booking end date and time. |
| `eventDate` | date | no | Event date and time for the booking. |
| `fax` | string | no | Booking fax number. |
| `firstName` | string | no | Booking contact first name. |
| `invoiceCategoryName` | string | no | Invoice category name for the booking. |
| `items[]` | array<object> | no | Array of items to include in the booking. |
| `items[].code` | string | no | Item code for one website booking line. |
| `items[].quantity` | number | no | Quantity for one website booking line. |
| `lastName` | string | no | Booking contact last name. |
| `message` | string | no | Customer-facing booking message. |
| `phone1` | string | no | Primary booking phone number. |
| `phone2` | string | no | Secondary booking phone number. |
| `phone3` | string | no | Third booking phone number. |
| `postcode` | string | no | Booking postcode. |
| `reference` | string | no | Booking reference text. |
| `state` | string | no | Booking state. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `branchCode` | string | no | Optional branch code when the Branches module is active. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native HirePOS API returns.

## Native endpoint

Through the native HirePOS API, this operation is `POST /WebsiteBookings` (base URL `https://api.hirepos.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-website-booking.md) for the provider-specific parameters and requirements.

