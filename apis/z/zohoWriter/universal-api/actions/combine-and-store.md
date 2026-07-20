# Zoho Writer: Combine And Store

Combines documents and stores them in Zoho Writer.

```
POST https://connect.mindcloud.co/v1/universal/zohoWriter/latest/actions/combine-and-store
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Writer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zohoWriter/latest/actions/combine-and-store" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoWriter/latest/actions/combine-and-store', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
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
| `outputSettings` | string | no | JSON string for optional output_settings such as name, folder_id, and overwrite_existing_file. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Zoho Writer API returns.

## Native endpoint

Through the native Zoho Writer API, this operation is `POST /v1/documents/pdf/combine/store` (base URL `{{credentials.accessTokenRequest.api_domain}}/writer/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/combine-and-store.md) for the provider-specific parameters and requirements.

