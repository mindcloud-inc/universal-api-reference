# Get Member with Patreon

Retrieves a member by ID from Patreon.

## Endpoint

- **Method:** `GET`
- **Path:** `/members/:memberId`
- **Base URL:** `https://www.patreon.com/api/oauth2/v2`
- **Official documentation:** [Get Member](https://docs.patreon.com#get-api-oauth2-v2-members-member_id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `memberId` | path | `string` | yes | The Patreon member ID. |
