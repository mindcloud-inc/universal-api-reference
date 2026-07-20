# Modusign: Get Template Embedded View URL

Retrieves an embedded template view URL from Modusign.

```
GET https://connect.mindcloud.co/v1/universal/modusign/latest/actions/get-template-embedded-view-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Modusign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/modusign/latest/actions/get-template-embedded-view-url?connectionId=$CONNECTION_ID&templateId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "templateId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/modusign/latest/actions/get-template-embedded-view-url?${params}`, {
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
| `templateId` | string | yes | The Modusign template ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "embeddedUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `embeddedUrl` | string | The embedded template edit URL. |

## Native endpoint

Through the native Modusign API, this operation is `GET /templates/:templateId/embedded-view` (base URL `https://api.modusign.co.kr`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-template-embedded-view-url.md) for the provider-specific parameters and requirements.

