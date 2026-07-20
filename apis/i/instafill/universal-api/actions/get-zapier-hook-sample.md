# Instafill: Get Zapier Hook Sample



```
GET https://connect.mindcloud.co/v1/universal/instafill/latest/actions/get-zapier-hook-sample
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Instafill `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/instafill/latest/actions/get-zapier-hook-sample?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/instafill/latest/actions/get-zapier-hook-sample?${params}`, {
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
| `eventType` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "converted_at": "string",
      "converted_pdf_url": "https://example.com",
      "form_id": "string",
      "job_id": "string",
      "review_url": "https://example.com",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `converted_at` | string | Example conversion timestamp emitted by the Zapier sample webhook. |
| `converted_pdf_url` | string | Example converted PDF URL emitted by the Zapier sample webhook. |
| `form_id` | string | Example form identifier emitted by the Zapier sample webhook. |
| `job_id` | string | Example Instafill conversion job identifier emitted by the Zapier sample webhook. |
| `review_url` | string | Example review URL emitted by the Zapier sample webhook. |
| `status` | string | Example status value emitted by the Zapier sample webhook. |

## Native endpoint

Through the native Instafill API, this operation is `GET /v1/integrations/zapier/hooks/sample` (base URL `https://api.instafill.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-zapier-hook-sample.md) for the provider-specific parameters and requirements.

