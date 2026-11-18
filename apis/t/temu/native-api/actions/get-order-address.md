# Get Order Address with Temu

Retrieve shipping address information for a specific order.

## Endpoint

- **Method:** `POST`
- **Path:** `/router`
- **Base URL:** `https://openapi-b-us.temu.com/openapi`
- **Official documentation:** [Get Order Address](https://partner-us.temu.com/documentation?menu_code=fb16b05f7a904765aac4af3a24b87d4a&sub_menu_code=ccc2f59661584f5e8e205d85ddb9a6c9)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `parentOrderSn` | body | `string` | yes | The parent order serial number - 'parentOrderSn' |
