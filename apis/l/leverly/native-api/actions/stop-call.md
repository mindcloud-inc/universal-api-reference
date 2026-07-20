# Stop Call with Leverly

## Endpoint

- **Method:** `POST`
- **Path:** `/inquiry/unpark`
- **Base URL:** `https://app.leverly.com/main`
- **Official documentation:** [Stop Call](https://leverly.com/kb/http-stop-calls/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `vendorLeadID` | body | `string` | no | Vendor lead ID from your system. It must have been included in the original post. |
| `Phone1` | body | `string` | no | Lead phone number in 1NNNNNNNNNN format. |
