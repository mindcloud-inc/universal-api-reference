# Get Availability with HirePOS

Retrieves item availability from HirePOS for a date range.

## Endpoint

- **Method:** `GET`
- **Path:** `/Availability`
- **Base URL:** `https://api.hirepos.com`
- **Official documentation:** [Get Availability](https://docs.hirepos.com/en/articles/2314625)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `DateFrom` | body | `date` | yes | Start of the requested availability window. |
| `DateTo` | body | `date` | yes | End of the requested availability window. |
| `Items[]` | body | `array<object>` | yes | Array of website-code items to check for availability. |
| `Items[].WebsiteCode` | body | `string` | yes | Website code for one item in the availability request. |
| `BranchID` | body | `number` | no | Optional branch ID for accounts using the Branches module. |
