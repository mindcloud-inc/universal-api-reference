# Create Group with TalentLMS

Creates a new group in TalentLMS.

## Endpoint

- **Method:** `POST`
- **Path:** `/groups`
- **Base URL:** `https://{domain}.talentlms.com/api/v2`
- **Official documentation:** [Create Group](https://documenter.getpostman.com/view/31867199/2sAY548Kou#create-a-group)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Group name. |
| `description` | body | `string` | no | Group description. |
| `key` | body | `string` | no | Group redemption key. |
| `max_key_redemptions` | body | `number` | no | Maximum key redemptions. |
| `price` | body | `number` | no | Group price. |
