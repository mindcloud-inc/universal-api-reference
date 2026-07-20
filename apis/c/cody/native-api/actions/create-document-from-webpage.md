# Create Document from Webpage with Cody

## Endpoint

- **Method:** `POST`
- **Path:** `/documents/webpage`
- **Base URL:** `https://getcody.ai/api/v1`
- **Official documentation:** [Create Document from Webpage](https://developers.meetcody.ai/operation/operation-create-document-from-webpage)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `folder_id` | body | `string` | no | Id of the folder to create the document in. |
| `url` | body | `string` | no | Valid publicly accessible webpage URL. |
