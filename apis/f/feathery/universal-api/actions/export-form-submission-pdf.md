# Feathery: Export Form Submission PDF



```
POST https://connect.mindcloud.co/v1/universal/feathery/latest/actions/export-form-submission-pdf
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Feathery `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/feathery/latest/actions/export-form-submission-pdf" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "form_id": "string",
  "user_id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/feathery/latest/actions/export-form-submission-pdf', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "form_id": "string",
    "user_id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `form_id` | string | yes | The unique ID of the form whose submission you want to export. |
| `user_id` | string | yes | The unique ID corresponding to the Feathery submission or user you want to export. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "pdf_url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `pdf_url` | string |  |

## Native endpoint

Through the native Feathery API, this operation is `POST /api/form/submission/pdf/` (base URL `https://api.feathery.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/export-form-submission-pdf.md) for the provider-specific parameters and requirements.

