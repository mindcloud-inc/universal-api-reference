# Add User to Branch with TalentLMS

Adds a user to a branch in TalentLMS.

## Endpoint

- **Method:** `POST`
- **Path:** `/branch-users`
- **Base URL:** `https://{domain}.talentlms.com/api/v2`
- **Official documentation:** [Add User to Branch](https://documenter.getpostman.com/view/31867199/2sAY548Kou#add-user-to-branch)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `branch_id` | body | `number` | yes | Numeric branch ID. |
| `user_id` | body | `number` | yes | Numeric user ID. |
