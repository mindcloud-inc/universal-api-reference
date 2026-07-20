# Zoho Writer: Combine And Deliver Via Webhook

Combines documents and delivers them via webhook in Zoho Writer.

```
POST https://connect.mindcloud.co/v1/universal/zohoWriter/latest/actions/combine-and-deliver-via-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Writer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zohoWriter/latest/actions/combine-and-deliver-via-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "webhook": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoWriter/latest/actions/combine-and-deliver-via-webhook', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "webhook": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `files` | file | no | PDF files to combine. Provide either files or urls; Zoho requires at least 2 PDFs and allows up to 20. Accepts multiple values as an array. |
| `files1` | file | no | Second PDF file to combine. Use together with files for the required two-file minimum. |
| `urls` | string | no | Comma-separated public PDF URLs to combine. Provide either urls or files. |
| `webhook` | string | yes | JSON string describing the required webhook target, including invoke_url and any optional retry or header fields. |
| `outputSettings` | string | no | JSON string for optional output_settings such as name and page_number_settings. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `status` | string |  |

## Native endpoint

Through the native Zoho Writer API, this operation is `POST /v1/documents/pdf/combine/webhook` (base URL `{{credentials.accessTokenRequest.api_domain}}/writer/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/combine-and-deliver-via-webhook.md) for the provider-specific parameters and requirements.

