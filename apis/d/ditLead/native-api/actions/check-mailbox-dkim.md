# Check Mailbox DKIM with DitLead

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/mailbox/check-dkim`
- **Base URL:** `https://api.ditlead.com`
- **Official documentation:** [Check Mailbox DKIM](https://ditlead.com/developer/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `domain` | body | `string` | yes | — |
| `domain` | body | `string` | yes | Domain to verify DKIM for. |
| `selector` | body | `string` | yes | — |
| `selector` | body | `string` | yes | DKIM selector to verify. |
