# Update Subscription with SimpleCirc

Updates an existing subscription in SimpleCirc.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1.2/subscribers/:account_id/subscriptions/:publication_id`
- **Base URL:** `https://simplecirc.com`
- **Official documentation:** [Update Subscription](https://simplecirc.com/docs/api)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `account_id` | path | `string` | yes |
| `publication_id` | path | `number` | yes |
| `status` | body | `string` | no |
| `issues_remaining` | body | `number` | no |
