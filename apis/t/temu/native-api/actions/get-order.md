# Get Order with Temu

Retrieve detailed information about a specific order.

## Endpoint

- **Method:** `POST`
- **Path:** `/router`
- **Base URL:** `https://openapi-b-us.temu.com/openapi`
- **Official documentation:** [Get Order](https://partner-us.temu.com/documentation?menu_code=fb16b05f7a904765aac4af3a24b87d4a&sub_menu_code=9bf33a25319e4d7bbaf5ece4b823b9c3)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `parentOrderSn` | body | `string` | yes | The parent order serial number - 'parentOrderSn' |
| `fulfillmentTypeList` | body | `list<string>` | no | The type of order fulfillment Send multiple values as a array. |
