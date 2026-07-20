# Remove User from Group with TalentLMS

Removes a user from a group in TalentLMS.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/group-memberships/`
- **Base URL:** `https://{domain}.talentlms.com/api/v2`
- **Official documentation:** [Remove User from Group](https://documenter.getpostman.com/view/31867199/2sAY548Kou#remove-user-from-a-group)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `group_id` | body | `number` | yes | Numeric group ID. |
| `user_id` | body | `number` | yes | Numeric user ID. |
