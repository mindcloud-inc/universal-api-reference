# Check Mailbox DMARC with DitLead

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/mailbox/check-dmarc`
- **Base URL:** `https://api.ditlead.com`
- **Official documentation:** [Check Mailbox DMARC](https://ditlead.com/developer/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `domain` | body | `string` | yes | — |
| `domain` | body | `string` | yes | Domain to verify DMARC for. |
