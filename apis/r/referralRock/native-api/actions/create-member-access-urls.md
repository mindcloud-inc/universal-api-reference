# Create Member Access URLs with Referral Rock

Creates member share and portal URLs in Referral Rock.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/memberaccessurls`
- **Base URL:** `https://api.referralrock.com`
- **Official documentation:** [Create Member Access URLs](https://api.referralrock.com/Help/Api/POST-api-memberaccessurls)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `expireInMinutes` | body | `number` | no | Number of minutes before the member access URLs expire. |
| `memberQuery` | body | `string` | yes | Check by member ID, referral code, email address, or external ID. |
