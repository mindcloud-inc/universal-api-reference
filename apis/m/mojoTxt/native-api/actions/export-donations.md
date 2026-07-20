# Export Donations with MojoTxt

Retrieves a donation export from MojoTxt.

## Endpoint

- **Method:** `GET`
- **Path:** `/:phoneNumber/donations/export/:donationIdOrKeyword`
- **Base URL:** `https://app.mojotxt.com/api/v1`
- **Official documentation:** [Export Donations](https://app.mojotxt.com/api/docs/v1/donations-export.php)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `donationIdOrKeyword` | path | `string` | yes | The donation keyword identifier or keyword value to export. |
| `EndTime` | query | `string` | no | Return donation transactions on or before this UNIX timestamp. |
| `GetPerson` | query | `string` | no | Set to 1 to include donor contact information in the export. |
| `phoneNumber` | path | `string` | yes | The MojoTxt phone number in international format, like +17792533748. |
| `StartTime` | query | `string` | no | Return donation transactions on or after this UNIX timestamp. |
