# Check Duplicate Person with Follow Up Boss

Finds duplicate people in Follow Up Boss by email or phone.

## Endpoint

- **Method:** `GET`
- **Path:** `people/checkDuplicate`
- **Base URL:** `https://api.followupboss.com/v1/`
- **Official documentation:** [Check Duplicate Person](https://docs.followupboss.com/reference/people-checkduplicate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | query | `string` | no | Email address to check for an existing person. |
| `phone` | query | `string` | no | Phone number to check for an existing person. |
