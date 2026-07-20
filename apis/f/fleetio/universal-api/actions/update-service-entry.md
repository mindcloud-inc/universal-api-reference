# Fleetio: Update Service Entry

Updates an existing service entry in Fleetio.

```
PUT https://connect.mindcloud.co/v1/universal/fleetio/latest/actions/update-service-entry
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fleetio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/fleetio/latest/actions/update-service-entry" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/fleetio/latest/actions/update-service-entry', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | The id of the relevant record |
| `completedAt` | date | no | The date and time at which the Service Entry was completed. We recommend using [ISO-8601](/docs/overview/date-formatting) formatted dates to avoid ambiguity. |
| `startedAt` | date | no | The date and time at which the Service Entry was started. We recommend using [ISO-8601](/docs/overview/date-formatting) formatted dates to avoid ambiguity. |
| `vehicleId` | number | no |  |
| `vehicleVin` | string | no | The VIN of the `Vehicle` associated with this Service Entry. |
| `vendorId` | number | no |  |
| `reference` | string | no | A reference number for this Service Entry. |
| `labelList` | string | no | A comma separated list of tags associated with this record. The only delimiter allowed is a comma (`,`). Please remove any commas from your labels before saving the record. |
| `generalNotes` | string | no | Any general notes about this Service Entry. |
| `vmrsRepairPriorityClassId` | number | no |  |
| `customFields` | object | no | *Full details on working with Custom Fields [here](/docs/overview/custom-fields). |
| `meterEntryAttributes` | object | no | A Service Entry may be associated with a [Meter Entry](/docs/api/meter-entries) |
| `secondaryMeterEntryAttributes` | object | no | A Service Entry may also be associated with a secondary [Meter Entry](/docs/api/meter-entries) |
| `serviceEntryLineItemsAttributes` | array<object> | no |  |
| `issueIds` | array<number> | no | The IDs of any Issues associated with this Service Entry. |
| `serviceTaskIds` | array<number> | no | The IDs of any Service Tasks associated with this Service Entry. |
| `commentsAttributes` | array<object> | no |  |
| `documentsAttributes` | array<object> | no | An array of one or more document objects to add to the record. Follow our [Attaching Documents and Images](/docs/overview/attaching-documents-and-images) guide to upload to our third party storage provider in order to obtain `file_url`. |
| `imagesAttributes` | array<object> | no | An array of one or more image objects to add to the record. Follow our [Attaching Documents and Images](/docs/overview/attaching-documents-and-images) guide to upload to our third party storage provider in order to obtain `file_url`. |
| `laborSubtotal` | number | no | The total cost of labor for this Service Entry. This is calculated by summing the `labor_cost` of each `Service Entry Line Item`. |
| `partsSubtotal` | number | no | The total cost of `Parts` for this Service Entry. This is calculated by summing the `parts_cost` of each `Service Entry Line Item`. |
| `subtotal` | number | no | The subtotal amount of this Service Entry before any discounts or taxes. This is calculated by summing the `subtotal` of each `Service Entry Line Item`. |
| `discount` | number | no | The total discount amount for this Service Entry. |
| `discountPercentage` | number | no | The total discount percentage for this Service Entry. |
| `discountType` | string | no | The type of discount applied to this record. |
| `tax1` | number | no | The first tax amount for this Service Entry. |
| `tax1Percentage` | number | no | The first tax percentage for this Service Entry. |
| `tax1Type` | string | no | The type of tax to apply to this record. |
| `tax2` | number | no | The second tax amount for this Service Entry. |
| `tax2Percentage` | number | no | The second tax percentage for this Service Entry. |
| `tax2Type` | string | no | The type of tax to apply to this record. |
| `totalAmount` | number | no | The grand total of this Service Entry. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Fleetio API returns.

## Native endpoint

Through the native Fleetio API, this operation is `PATCH service_entries/:id` (base URL `https://secure.fleetio.com/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-service-entry.md) for the provider-specific parameters and requirements.

