# Refund Order Lines with Walmart

Issue refunds for return orders.

## Endpoint

- **Method:** `POST`
- **Path:** `/v3/returns/:returnOrderId/refund`
- **Base URL:** `https://{environment}.walmartapis.com`
- **API:** REST
- **Official documentation:** [Refund Order Lines](https://developer.walmart.com/us-marketplace/reference/issuerefund)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json; charset=utf-8` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `refundLines` | body | `array<object>` | no | List of return order lines to refund. |
| `refundLines[].quantity.measurementValue` | body | `number` | no | Numeric value for the quantity in the specified unit of measure. |
| `refundLines[].returnOrderLineNumber` | body | `number` | no | Line number within the return order. Required when the return order contains multiple lines. If the return order contains a single line and this field is not sent, that line is selected automatically. Omitting a required line number results in a data error. |
| `returnOrderId` | path | `string` | yes | Return order identifier also known as RMA number. |
| `refundLines[].quantity` | body | `object` | no | Quantity to refund on this return line. |
| `refundLines[].quantity.unitOfMeasure` | body | `list<string>` | no | Unit of measure for the quantity. Examples include `EACH` or `EA`. |
| `isDynamicSandbox` | query | `boolean` | no | — |
| `customerOrderId` | body | `string` | yes | — |
