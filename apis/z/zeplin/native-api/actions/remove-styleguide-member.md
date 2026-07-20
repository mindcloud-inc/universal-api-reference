# Remove Styleguide Member with Zeplin

Removes a member from a Zeplin styleguide.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/styleguides/{styleguide_id}/members/{member_id}`
- **Base URL:** `https://api.zeplin.dev/v1`
- **Official documentation:** [Remove Styleguide Member](https://docs.zeplin.dev/reference/removestyleguidemember)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `styleguide_id` | path | `string` | yes | Styleguide id |
| `member_id` | path | `string` | yes | Member id |
