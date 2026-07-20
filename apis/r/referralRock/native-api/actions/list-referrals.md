# List Referrals with Referral Rock

Retrieves referral records from Referral Rock.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/referrals`
- **Base URL:** `https://api.referralrock.com`
- **Official documentation:** [List Referrals](https://api.referralrock.com/Help/Api/GET-api-referrals_programId_query_memberId_sort_dateFrom_dateTo_status_offset_count)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `dateFrom` | query | `date` | no | Show referrals created after this date. |
| `dateTo` | query | `date` | no | Show referrals created before this date. |
| `memberId` | query | `string` | no | Filter referrals by member ID. |
| `programId` | query | `string` | no | ID of the program, program name, or program title. |
| `query` | query | `string` | no | Filter referrals by email, internal ID, external ID, or referral code. |
| `sort` | query | `string` | no | Column to sort by. |
| `status` | query | `string` | no | Filter referrals by status: pending, qualified, approved, or denied. |
