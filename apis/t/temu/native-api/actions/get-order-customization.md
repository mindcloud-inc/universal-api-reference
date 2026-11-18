# Get Order Customization with Temu

Retrieve customized product content information in bulk

## Endpoint

- **Method:** `POST`
- **Path:** `/router`
- **Base URL:** `https://openapi-b-us.temu.com/openapi`
- **Official documentation:** [Get Order Customization](https://partner-us.temu.com/documentation?menu_code=fb16b05f7a904765aac4af3a24b87d4a&sub_menu_code=e8f86a2f5241441e9b095bf309d04dce)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `orderSnList` | body | `string` | no | One or more Order Serial Numbers - 'orderSnList["string"]'  **Up to 10 Orders can be queried at once.** Send multiple values as a array. |
