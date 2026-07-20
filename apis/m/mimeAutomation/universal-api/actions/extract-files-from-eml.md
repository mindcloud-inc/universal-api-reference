# Mime Automation: Extract Files From EML

Retrieves attachments from a base64-encoded EML file in Mime Automation.

```
GET https://connect.mindcloud.co/v1/universal/mimeAutomation/latest/actions/extract-files-from-eml
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mime Automation `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mimeAutomation/latest/actions/extract-files-from-eml?connectionId=$CONNECTION_ID&content=Paste%20base64-encoded%20EML%20content" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "content": "Paste base64-encoded EML content"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mimeAutomation/latest/actions/extract-files-from-eml?${params}`, {
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
| `content` | string | yes | Base64-encoded string of an EML file. Example: `Paste base64-encoded EML content`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "content": "string",
      "fileName": "Ava Chen",
      "mimeType": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `content` | string | Base64-encoded attachment file content. |
| `fileName` | string | File name with extension. |
| `mimeType` | string | Content or media type, for example image/png. |

## Native endpoint

Through the native Mime Automation API, this operation is `POST /MimeAutomation/ExtractFilesFromEml` (base URL `https://accloudsolutions.p.nadles.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/extract-files-from-eml.md) for the provider-specific parameters and requirements.

