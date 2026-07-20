# Skip Documents with Parsio

## Endpoint

- **Method:** `POST`
- **Path:** `/mailboxes/:mailbox_id/docs/skip`
- **Base URL:** `https://api.parsio.io`
- **Official documentation:** [Skip Documents](https://help.parsio.io/public-api/parsio-public-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `mailbox_id` | path | `string` | yes | Parsio mailbox ID. |
| `ids[]` | body | `array<string>` | yes | Document IDs to skip. |
