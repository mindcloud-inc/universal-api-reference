# Check Mailbox SPF with DitLead

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/mailbox/check-spf`
- **Base URL:** `https://api.ditlead.com`
- **Official documentation:** [Check Mailbox SPF](https://ditlead.com/developer/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `domain` | body | `string` | yes | — |
| `domain` | body | `string` | yes | Domain to verify SPF for. |
