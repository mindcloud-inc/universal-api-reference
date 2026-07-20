# Get Manager By Phone Number with SalesDrive

Retrieves manager and contact details by phone number in SalesDrive.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/get_manager_by_phone_number/`
- **Base URL:** `https://{account}.salesdrive.me`
- **Official documentation:** [Get Manager By Phone Number](https://api.salesdrive.me/api/docs/#/call/call-manager)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `phone` | query | `string` | yes | Phone number to search for. |
