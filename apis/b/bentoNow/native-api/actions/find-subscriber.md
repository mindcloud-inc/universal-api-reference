# Find Subscriber with Bento Now

Finds a subscriber in Bento Now by email or UUID.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/fetch/subscribers`
- **Base URL:** `https://app.bentonow.com/api`
- **Official documentation:** [Find Subscriber](https://bentonow.com/docs/subscribers)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `email` | query | `string` | yes |
| `uuid` | query | `string` | no |
