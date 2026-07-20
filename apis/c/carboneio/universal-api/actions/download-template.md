# Carbone.io: Download Template

Downloads a template from Carbone.io.

```
GET https://connect.mindcloud.co/v1/universal/carboneio/latest/actions/download-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Carbone.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/carboneio/latest/actions/download-template?connectionId=$CONNECTION_ID&templateIdOrVersionId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "templateIdOrVersionId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/carboneio/latest/actions/download-template?${params}`, {
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
| `templateIdOrVersionId` | string | yes | Template ID (64-bit) or Version ID (SHA-256) to download. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "response": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `response` | string | Raw template file contents returned by Carbone. |

## Native endpoint

Through the native Carbone.io API, this operation is `GET /template/[:templateId-or-versionId]` (base URL `https://api.carbone.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/download-template.md) for the provider-specific parameters and requirements.

