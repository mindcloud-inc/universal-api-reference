# Create Member with Memberstack

## Endpoint

- **Method:** `POST`
- **Path:** `/members`
- **Base URL:** `https://admin.memberstack.com`
- **Official documentation:** [Create Member](https://developers.memberstack.com/admin-rest-api/member-actions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | Member email address for the new member. |
| `password` | body | `string` | yes | Password for the new member (minimum 8 characters). |
