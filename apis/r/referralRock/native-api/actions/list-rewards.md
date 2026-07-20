# List Rewards with Referral Rock

Retrieves reward records from Referral Rock.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/rewards`
- **Base URL:** `https://api.referralrock.com`
- **Official documentation:** [List Rewards](https://api.referralrock.com/Help/Api/GET-api-rewards_programId_memberId_query_status_sort_dateFrom_dateTo_offset_count)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `dateFrom` | query | `date` | no | Show rewards created after this date. |
| `dateTo` | query | `date` | no | Show rewards created before this date. |
| `memberId` | query | `string` | no | ID of the member. |
| `programId` | query | `string` | no | ID of the program, program name, or program title. |
| `query` | query | `string` | no | Filter the recipient by email, ID, external ID, or member referral code. |
| `sort` | query | `string` | no | Column to sort by. |
| `status` | query | `string` | no | Filter rewards by status. |
