# Create Website Booking with HirePOS

Creates a new website booking in HirePOS.

## Endpoint

- **Method:** `POST`
- **Path:** `/WebsiteBookings`
- **Base URL:** `https://api.hirepos.com`
- **Official documentation:** [Create Website Booking](https://docs.hirepos.com/en/articles/2314369)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `AddressLine1` | body | `string` | no | Primary booking address line. |
| `AddressLine2` | body | `string` | no | Secondary booking address line. |
| `BookingDate` | body | `date` | no | Booking date for the website booking. |
| `BranchCode` | body | `string` | no | Optional branch code when the Branches module is active. |
| `City` | body | `string` | no | Booking city. |
| `Comments` | body | `string` | no | Internal booking comments. |
| `Company` | body | `string` | no | Booking company name. |
| `Country` | body | `string` | no | Booking country. |
| `CustomField1` | body | `string` | no | Custom website booking field 1. |
| `CustomField2` | body | `string` | no | Custom website booking field 2. |
| `CustomField3` | body | `string` | no | Custom website booking field 3. |
| `CustomField4` | body | `string` | no | Custom website booking field 4. |
| `CustomField5` | body | `string` | no | Custom website booking field 5. |
| `CustomField6` | body | `string` | no | Custom website booking field 6. |
| `CustomField7` | body | `string` | no | Custom website booking field 7. |
| `CustomField8` | body | `string` | no | Custom website booking field 8. |
| `DeliveryAddressLine1` | body | `string` | no | Primary delivery address line. |
| `DeliveryAddressLine2` | body | `string` | no | Secondary delivery address line. |
| `DeliveryCity` | body | `string` | no | Delivery city. |
| `DeliveryPostcode` | body | `string` | no | Delivery postcode. |
| `DeliveryState` | body | `string` | no | Delivery state. |
| `Email` | body | `string` | no | Booking email address. |
| `EstDateFrom` | body | `date` | no | Estimated booking start date and time. |
| `EstDateTo` | body | `date` | no | Estimated booking end date and time. |
| `EventDate` | body | `date` | no | Event date and time for the booking. |
| `Fax` | body | `string` | no | Booking fax number. |
| `FirstName` | body | `string` | no | Booking contact first name. |
| `InvoiceCategoryName` | body | `string` | no | Invoice category name for the booking. |
| `Items[]` | body | `array<object>` | no | Array of items to include in the booking. |
| `Items[].Code` | body | `string` | no | Item code for one website booking line. |
| `Items[].Quantity` | body | `number` | no | Quantity for one website booking line. |
| `LastName` | body | `string` | no | Booking contact last name. |
| `Message` | body | `string` | no | Customer-facing booking message. |
| `Phone1` | body | `string` | no | Primary booking phone number. |
| `Phone2` | body | `string` | no | Secondary booking phone number. |
| `Phone3` | body | `string` | no | Third booking phone number. |
| `Postcode` | body | `string` | no | Booking postcode. |
| `Reference` | body | `string` | no | Booking reference text. |
| `State` | body | `string` | no | Booking state. |
