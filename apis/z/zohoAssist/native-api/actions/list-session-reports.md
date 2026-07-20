# List Session Reports with Zoho Assist

Lists reports for previously conducted Zoho Assist sessions.

## Endpoint

- **Method:** `GET`
- **Path:** `/reports`
- **Base URL:** `https://assist.zoho.com/api/v2`
- **Official documentation:** [List Session Reports](https://www.zoho.com/assist/api/getsessionreports.html)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `type` | query | `string` | yes | Report type: rs, URS, or all. |
| `fromdate` | query | `number` | yes | Report start time in Unix milliseconds. |
| `todate` | query | `number` | yes | Report end time in Unix milliseconds. |
| `email` | query | `string` | no | Filter reports to a technician email. |
