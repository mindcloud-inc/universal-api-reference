# Unbounce: Create Page Lead

Creates a lead for an Unbounce page.

```
POST https://connect.mindcloud.co/v1/universal/unbounce/latest/actions/create-page-lead
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Unbounce `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/unbounce/latest/actions/create-page-lead" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "form_submission": "[object Object]",
  "page_id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/unbounce/latest/actions/create-page-lead', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "form_submission": "[object Object]",
    "page_id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `form_submission` | object | yes | Lead submission payload. Include variant_id and form_data field arrays. Example: `[object Object]`. |
| `page_id` | string | yes | Unbounce page ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "extraData": {},
      "formData": {},
      "id": "string",
      "metadata": {},
      "pageId": "string",
      "variantId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string |  |
| `extraData` | object |  |
| `formData` | object |  |
| `id` | string |  |
| `metadata` | object |  |
| `pageId` | string |  |
| `variantId` | string |  |

## Native endpoint

Through the native Unbounce API, this operation is `POST /pages/:page_id/leads` (base URL `https://api.unbounce.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-page-lead.md) for the provider-specific parameters and requirements.

