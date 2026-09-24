# List Worker Time Off Balances with ADP

## Endpoint

- **Method:** `GET`
- **Path:** `time/v2/workers/:aoid/time-off-details/time-off-balances`
- **Base URL:** `https://api.adp.com/`
- **Official documentation:** [List Worker Time Off Balances](https://marketplace-cdn.adp.com/dev-portal/pdf/protected/Time_Off_Balances_API_Guide_for_ADP_Workforce_Now)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `aoid` | path | `string` | yes | The ADP associate object identifier for the worker whose time-off balances should be returned. |
