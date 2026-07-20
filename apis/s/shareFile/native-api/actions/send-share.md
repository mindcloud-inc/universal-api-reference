# Send Share with ShareFile

## Endpoint

- **Method:** `POST`
- **Path:** `/Shares/Send`
- **Base URL:** `https://{subdomain}.{apicp}/sf/v3`
- **Official documentation:** [Send Share](https://api.sharefile.com/html/docs/Shares.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Subject` | body | `string` | yes | The email subject for the sent share. |
| `Items[]` | body | `array<string>` | yes | The list of item identifiers to include in the sent share. |
| `Emails[]` | body | `array<string>` | yes | The recipient email addresses for the sent share. |
