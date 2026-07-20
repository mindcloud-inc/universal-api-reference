# Email Extract Metadata with Encodian

Retrieves email metadata from Encodian.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/General/GetEmailInfo`
- **Base URL:** `https://api.apps-encodian.com`
- **Official documentation:** [Email Extract Metadata](https://support.encodian.com/hc/en-gb/articles/12237799140252)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fileContent` | body | `string` | yes | A Base64 encoded representation of the email file to be processed. |
| `cultureName` | body | `string` | no | Set the culture for the document prior to conversion. |
