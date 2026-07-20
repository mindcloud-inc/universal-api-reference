# Get 5-Minute Prices By Time Range with ComEd

Retrieves 5-minute prices from ComEd for a time range.

## Endpoint

- **Method:** `GET`
- **Path:** `/api`
- **Base URL:** `https://hourlypricing.comed.com`
- **Official documentation:** [Get 5-Minute Prices By Time Range](https://hourlypricing.comed.com/hp-api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `datestart` | query | `string` | yes | Inclusive start timestamp in the documented ComEd format YYYYMMDDhhmm. |
| `dateend` | query | `string` | yes | Inclusive end timestamp in the documented ComEd format YYYYMMDDhhmm. |
