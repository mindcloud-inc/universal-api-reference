# List Members with Referral Rock

Retrieves referral program members from Referral Rock.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/members`
- **Base URL:** `https://api.referralrock.com`
- **Official documentation:** [List Members](https://api.referralrock.com/Help/Api/GET-api-members_programId_query_showDisabled_sort_dateFrom_dateTo_offset_count)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `dateFrom` | query | `date` | no | Show members created after this date. |
| `dateTo` | query | `date` | no | Show members created before this date. |
| `programId` | query | `string` | no | ID of the program, program name, or program title. |
| `query` | query | `string` | no | Filter members by email, internal ID, external ID, or referral code. |
| `showDisabled` | query | `boolean` | no | Set true to include disabled members. |
| `sort` | query | `string` | no | Column to sort by. |
