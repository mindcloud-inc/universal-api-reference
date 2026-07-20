# Mime Automation: Extract Files From TNEF

Retrieves attachments from a TNEF-encoded file in Mime Automation.

```
GET https://connect.mindcloud.co/v1/universal/mimeAutomation/latest/actions/extract-files-from-tnef
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mime Automation `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mimeAutomation/latest/actions/extract-files-from-tnef?connectionId=$CONNECTION_ID&content=Paste%20base64-encoded%20TNEF%20content" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "content": "Paste base64-encoded TNEF content"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mimeAutomation/latest/actions/extract-files-from-tnef?${params}`, {
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
| `content` | string | yes | Base64-encoded string of a TNEF file, such as winmail.dat. Example: `Paste base64-encoded TNEF content`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "content": "string",
      "fileName": "Ava Chen"
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

## Native endpoint

Through the native Mime Automation API, this operation is `POST /MimeAutomation/ExtractFiles` (base URL `https://accloudsolutions.p.nadles.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/extract-files-from-tnef.md) for the provider-specific parameters and requirements.

