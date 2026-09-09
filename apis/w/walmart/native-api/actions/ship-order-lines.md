# Ship Order Lines with Walmart

Marks specified order lines in a single purchase order as shipped.

## Endpoint

- **Method:** `POST`
- **Path:** `/v3/orders/:purchaseOrderId/shipping`
- **Base URL:** `https://{environment}.walmartapis.com`
- **API:** REST
- **Official documentation:** [Ship Order Lines](https://developer.walmart.com/us-marketplace/reference/acknowledgeorders)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json; charset=utf-8` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `purchaseOrderId` | path | `string` | yes | Unique Walmart purchaseOrderId that identifies the purchase order. |
| `processMode` | body | `string` | no | Optional. If updating tracking info after shipment, set this fields value to: PARTIAL_UPDATE to indicate a partial update of shipping information. |
| `userInputLines[].lineNumber` | body | `string` | no | Identifier of the specific order line to be cancelled. |
| `userInputLines[].trackingInfo.carrier` | body | `list<string>` | no | The package shipment carrier. Valid entries are: UPS, USPS, FedEx, Airborne, OnTrac, DHL Ecommerce - US, DHL, LS (LaserShip), UDS (United Delivery Service), UPSMI (UPS Mail Innovations), FDX, PILOT, ESTES, SAIA, FDS Express, Seko Worldwide, HIT Delivery, FEDEXSP (FedEx SmartPost), RL Carriers, Metropolitan Warehouse & Delivery, China Post, YunExpress,Yellow Freight Sys, AIT Worldwide Logistics, Chukou1, Sendle, Landmark Global, Sunyou, Yanwen, 4PX, GLS, OSM Worldwide, FIRST MILE, AM Trucking, CEVA, India Post, SF Express, CNE, TForce Freight, AxleHire, LSO, Royal Mail, ABF Freight System, WanB, Roadrunner Freight, Meyer Distribution, AAA Cooper, Canada Post, Southeastern Freight Lines, Japan Post, Correos de Mexico, XPO Logistics, JD Logistics, YDH, JCEX, Flyt, Deutsche Post, Better Trucks, Asendia, SFC, UBI, ePost Global, YF Logistics, RXO, Estes Express, Shypmax, WIN.IT America, PITT OHIO, PostNord Sweden, Equick, Whistl, Tusou, Shiprocket, DTDC, PTS. |
| `dynamicSandbox` | path | `boolean` | no | — |
| `userInputLines[]` | body | `array<object>` | no | Array of objects, each specifying cancellation details for an individual order line. |
| `userInputLines[].intentToCancelOverride` | body | `boolean` | no | Optional. If the customer has requested cancellation, toggle on to confirm you still intend to ship the order. Format: `toggle`. |
| `userInputLines[].trackingInfo.otherCarrier` | body | `string` | no | Custom name for a shipping carrier when the carrier is not one of the predefined options; if used, a valid trackingURL must also be provided. |
| `userInputLines[].sellerOrderId` | body | `string` | no | Seller-defined order ID (max 30 characters). Walmart prints this ID on return labels so the seller can reference the sales order. |
| `userInputLines[].trackingInfo.methodCode` | body | `string` | no | Shipping service level for the package (such as Standard, Express, OneDay, WhiteGlove, Value, Freight), indicating delivery speed or handling. |
| `userInputLines[].sellerOrderNo` | body | `string` | no | Seller’s unique purchase order number for this order, used internally when creating or updating orders. |
| `userInputLines[].trackingInfo.trackingNumber` | body | `string` | no | Current alphanumeric identifier assigned by the carrier, used to update the purchase order’s tracking status. |
| `userInputLines[].trackingInfo.trackingURL` | body | `string` | no | URL where the shipment status can be tracked online. Mandatory when using a custom otherCarrier name. |
| `userInputLines[].trackingInfo.shipDateTime` | body | `date` | no | Timestamp in UNIX epoch (int64) format representing the exact date and time the package was shipped. |
| `userInputLines[].unitOfMeasurement` | body | `list<string>` | no | Unit of measure for the status quantity (such as EACH or EA), defining how the amount is counted. |
| `userInputLines[].amount` | body | `number` | no | Numeric value representing how many units fall into the specified status category. |
| `userInputLines[].trackingInfo` | body | `object` | no | Object containing shipment and tracking details for the package, including carrier information, shipping method, shipment timestamp, tracking number, and optional tracking URL' |
