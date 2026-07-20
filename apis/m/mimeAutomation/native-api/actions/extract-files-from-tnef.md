# Extract Files From TNEF with Mime Automation

Retrieves attachments from a TNEF-encoded file in Mime Automation.

## Endpoint

- **Method:** `POST`
- **Path:** `/MimeAutomation/ExtractFiles`
- **Base URL:** `https://accloudsolutions.p.nadles.com`
- **Official documentation:** [Extract Files From TNEF](https://learn.microsoft.com/en-us/connectors/mimeautomationip/#extract-files-from-a-tnef-encoded-file)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `content` | body | `string` | yes | Base64-encoded string of a TNEF file, such as winmail.dat. |
