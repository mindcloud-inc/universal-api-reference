# Dropbox Sign: Get Embedded Template Edit URL

Retrieves an embedded template edit URL from Dropbox Sign.

```
GET https://connect.mindcloud.co/v1/universal/dropboxSign/latest/actions/get-embedded-template-edit-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dropbox Sign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dropboxSign/latest/actions/get-embedded-template-edit-url?connectionId=$CONNECTION_ID&template_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "template_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dropboxSign/latest/actions/get-embedded-template-edit-url?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `allow_edit_ccs` | boolean | no | Whether users can add or change CC roles while editing the template. |
| `force_signer_roles` | boolean | no | Whether users can review and edit signer roles. |
| `force_subject_message` | boolean | no | Whether users can review and edit the subject and message. |
| `preview_only` | boolean | no | Whether to allow preview without letting the user add fields. |
| `show_preview` | boolean | no | Whether to enable the editor preview experience. |
| `template_id` | string | yes | The id of the template to edit. |
| `test_mode` | boolean | no | Whether to edit a locked embedded template in test mode. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Dropbox Sign API returns.

## Native endpoint

Through the native Dropbox Sign API, this operation is `POST /embedded/edit_url/:template_id` (base URL `https://api.hellosign.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-embedded-template-edit-url.md) for the provider-specific parameters and requirements.

