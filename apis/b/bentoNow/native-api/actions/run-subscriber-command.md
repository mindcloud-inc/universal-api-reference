# Run Subscriber Command with Bento Now

Runs a targeted subscriber command in Bento Now.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/fetch/commands`
- **Base URL:** `https://app.bentonow.com/api`
- **Official documentation:** [Run Subscriber Command](https://bentonow.com/docs/subscribers)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `command.command` | body | `string` | yes |
| `command.email` | body | `string` | yes |
| `command.query` | body | `string` | yes |
