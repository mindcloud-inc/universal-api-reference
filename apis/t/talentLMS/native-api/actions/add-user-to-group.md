# Add User to Group with TalentLMS

Adds a user to a group in TalentLMS.

## Endpoint

- **Method:** `POST`
- **Path:** `/group-memberships/`
- **Base URL:** `https://{domain}.talentlms.com/api/v2`
- **Official documentation:** [Add User to Group](https://documenter.getpostman.com/view/31867199/2sAY548Kou#add-a-user-to-a-group)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `group_id` | body | `number` | yes | Numeric group ID. |
| `user_id` | body | `number` | yes | Numeric user ID. |
