# Get Attachment / File with Ragic

Retrieves an attachment or file from Ragic.

## Endpoint

- **Method:** `GET`
- **Path:** `{serverUrl}/file.jsp`
- **Base URL:** `{serverUrl}/mindcloud`
- **Official documentation:** [Get Attachment / File](https://www.ragic.com/docs/api/en/#tag/reading-files)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `a` | query | `string` | yes | Ragic account name used in the download URL. |
| `f` | query | `string` | yes | Attachment token returned by Ragic record data, including the prefix before the @ symbol. |
