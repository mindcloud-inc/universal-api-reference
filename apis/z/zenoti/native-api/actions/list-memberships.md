# Get Memberships Report with Zenoti

## Endpoint

- **Method:** `POST`
- **Path:** `reports/memberships/flat_file`
- **Base URL:** `https://api.zenoti.com/v1/`
- **Official documentation:** [Get Memberships Report](None)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `centers[]` | body | `array` | no | — |
| `centers[].center` | body | `list` | no | — |
| `membershipType[].type` | body | `list` | no | — |
| `status[].status` | body | `list` | no | Format: `toggle`. |
| `date_type` | body | `list` | no | — |
| `start_date` | body | `date` | no | — |
| `end_date` | body | `date` | no | — |
| `liability_type` | body | `list` | no | — |
| `grace_period` | body | `boolean` | no | Format: `toggle`. |
| `status[]` | body | `array` | no | Format: `toggle`. |
| `membershipType[]` | body | `array` | no | — |
| `includeTotal` | body | `boolean` | no | Format: `toggle`. |
