# Extract Files From EML with Mime Automation

Retrieves attachments from a base64-encoded EML file in Mime Automation.

## Endpoint

- **Method:** `POST`
- **Path:** `/MimeAutomation/ExtractFilesFromEml`
- **Base URL:** `https://accloudsolutions.p.nadles.com`
- **Official documentation:** [Extract Files From EML](https://learn.microsoft.com/en-us/connectors/mimeautomationip/#extract-files-from-a-base64-encoded-eml-file)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `content` | body | `string` | yes | Base64-encoded string of an EML file. |
