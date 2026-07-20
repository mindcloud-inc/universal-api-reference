# Get Package Detail with TikTok Shop

Returns information about a package, including handover time slot, tracking number, and shipping provider information.

## Endpoint

- **Method:** `GET`
- **Path:** `fulfillment/202309/packages/:packageID`
- **Base URL:** `https://open-api.tiktokglobalshop.com/`
- **Official documentation:** [Get Package Detail](https://partner.tiktokshop.com/docv2/page/get-package-detail-202309#Back%20To%20Top)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `packageID` | path | `string` | yes |
| `shop_cipher` | query | `list<string>` | no |
