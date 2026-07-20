# Create or Update Person with Hy.page

## Endpoint

- **Method:** `POST`
- **Path:** `/hyax-api/v1/people/add`
- **Base URL:** `https://platform.hyax.com`
- **Official documentation:** [Create or Update Person](https://platform.hyax.com/api-docs/people-add)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `city` | body | `string` | no | City. |
| `country` | body | `string` | no | Country. |
| `email` | body | `string` | yes | Trimmed, lowercased person email. |
| `notes` | body | `string` | no | Notes stored in metadata. |
| `phone` | body | `string` | no | Phone number. |
| `referrer` | body | `string` | no | Referrer URL, max 1000 characters. |
| `state` | body | `string` | no | State. |
| `utm_source` | body | `string` | no | UTM source, max 200 characters. |
| `name` | body | `string` | no | Display name. |
| `tags` | body | `string` | no | Tags merged with existing tags on update. |
| `purchaseValue` | body | `number` | no | Purchase value. Validation error if NaN. |
| `source` | body | `string` | no | Signup source. Defaults to API on create. |
