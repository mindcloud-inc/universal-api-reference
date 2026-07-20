# Invite User to Vybit with Vybit

## Endpoint

- **Method:** `POST`
- **Path:** `/peep/{{key}}`
- **Base URL:** `https://api.vybit.net/v1`
- **Official documentation:** [Invite User to Vybit](https://developer.vybit.net/api-reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | Email address of the user to invite to the vybit. |
| `key` | path | `string` | yes | The unique key of the vybit to invite a user to. |
