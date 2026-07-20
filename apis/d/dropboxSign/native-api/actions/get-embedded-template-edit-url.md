# Get Embedded Template Edit URL with Dropbox Sign

Retrieves an embedded template edit URL from Dropbox Sign.

## Endpoint

- **Method:** `POST`
- **Path:** `/embedded/edit_url/:template_id`
- **Base URL:** `https://api.hellosign.com/v3`
- **Official documentation:** [Get Embedded Template Edit URL](https://developers.hellosign.com/api/reference/operation/embeddedEditUrl/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `allow_edit_ccs` | body | `boolean` | no | Whether users can add or change CC roles while editing the template. |
| `force_signer_roles` | body | `boolean` | no | Whether users can review and edit signer roles. |
| `force_subject_message` | body | `boolean` | no | Whether users can review and edit the subject and message. |
| `preview_only` | body | `boolean` | no | Whether to allow preview without letting the user add fields. |
| `show_preview` | body | `boolean` | no | Whether to enable the editor preview experience. |
| `template_id` | path | `string` | yes | The id of the template to edit. |
| `test_mode` | body | `boolean` | no | Whether to edit a locked embedded template in test mode. |
