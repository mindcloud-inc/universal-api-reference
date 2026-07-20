# Transloadit: Delete Template

Deletes an existing template from Transloadit.

```
DELETE https://connect.mindcloud.co/v1/universal/transloadit/latest/actions/delete-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Transloadit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/transloadit/latest/actions/delete-template?connectionId=$CONNECTION_ID&templateId=string&params=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "templateId": "string",
  "params": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/transloadit/latest/actions/delete-template?${params}`, {
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
| `templateId` | string | yes | The ID of the template to delete. |
| `params` | string | yes | JSON string required by Transloadit for template deletion requests. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "ok": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string | Human-readable result message. |
| `ok` | string | Status code returned by Transloadit for template deletion. |

## Native endpoint

Through the native Transloadit API, this operation is `DELETE /templates/:templateId` (base URL `https://api2.transloadit.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-template.md) for the provider-specific parameters and requirements.

