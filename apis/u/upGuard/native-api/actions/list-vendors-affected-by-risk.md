# List Vendors Affected By Risk with UpGuard

Retrieves vendors affected by a risk in UpGuard.

## Endpoint

- **Method:** `GET`
- **Path:** `/risks/vendors_with_risk`
- **Base URL:** `https://cyber-risk.upguard.com/api/public`
- **Official documentation:** [List Vendors Affected By Risk](https://cyber-risk.upguard.com/api/docs#operation/get_vendors_with_risk_params)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `risk_id` | query | `string` | yes | The risk ID to filter by. |
