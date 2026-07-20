# List Unattended Computers with Zoho Assist

Lists unattended computers configured in Zoho Assist.

## Endpoint

- **Method:** `GET`
- **Path:** `/devices`
- **Base URL:** `https://assist.zoho.com/api/v2`
- **Official documentation:** [List Unattended Computers](https://www.zoho.com/assist/api/getunattendedcomputer.html)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `departmentId` | path | `string` | yes |
| `source` | path | `string` | no |
