# Remove User from Branch with TalentLMS

Removes a user from a branch in TalentLMS.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/branch-users`
- **Base URL:** `https://{domain}.talentlms.com/api/v2`
- **Official documentation:** [Remove User from Branch](https://documenter.getpostman.com/view/31867199/2sAY548Kou#remove-user-from-branch)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `branch_id` | body | `number` | yes | Numeric branch ID. |
| `user_id` | body | `number` | yes | Numeric user ID. |
