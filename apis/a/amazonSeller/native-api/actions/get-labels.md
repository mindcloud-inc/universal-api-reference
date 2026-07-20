# Get Labels with Amazon Seller

Retrieves inbound shipment labels from Amazon Seller.

## Endpoint

- **Method:** `GET`
- **Path:** `fba/inbound/v0/shipments/:shipmentId/label`
- **Base URL:** `https://{environment}-{region}.amazon.com`
- **API:** PageSize / PageStartIndex
- **Official documentation:** [Get Labels](https://developer-docs.amazon.com/sp-api/reference/getlabels)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `shipmentId` | path | `string` | yes | A shipment identifier originally returned by the `createInboundShipmentPlan` operation. |
| `PageType` | query | `list<string>` | yes | The page type to use to print the labels. Submitting a PageType value that is not supported in your marketplace returns an error. |
| `LabelType` | query | `list<string>` | yes | The type of labels being requested. |
| `NumberOfPackages` | query | `number` | no | The number of packages in the shipment. (optional) |
| `NumberOfPallets` | query | `number` | no | The number of pallets in the shipment. This returns four identical labels for each pallet. |
| `PackageLabelsToPrint` | query | `string` | no | A list of identifiers that specify packages for which you want package labels printed.  Note: ``` If you provide box content information with the FBA Inbound Shipment Carton Information Feed, then PackageLabelsToPrint must match the CartonId values you provide through that feed. If you provide box content information with the Fulfillment Inbound API v2024-03-20, then PackageLabelsToPrint must match the boxID values from the listShipmentBoxes response. If these values do not match as required, the operation returns the IncorrectPackageIdentifier error code. ``` Send multiple values as a array. |
