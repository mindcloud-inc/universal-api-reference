# PostGrid Print & Mail: Create Template

Creates a template in PostGrid Print & Mail.

```
POST https://connect.mindcloud.co/v1/universal/postGridPrintMail/latest/actions/create-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PostGrid Print & Mail `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/postGridPrintMail/latest/actions/create-template" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/postGridPrintMail/latest/actions/create-template', {
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
| `html` | string | no | The HTML content for the template. |
| `description` | string | no | An optional description visible in the API and dashboard. |
| `metadata` | object | no | Custom metadata for this template. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archived": true,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "html": "string",
      "id": "string",
      "live": true,
      "metadata": {},
      "object": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archived` | boolean |  |
| `createdAt` | date |  |
| `description` | string |  |
| `html` | string |  |
| `id` | string |  |
| `live` | boolean |  |
| `metadata` | object |  |
| `object` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native PostGrid Print & Mail API, this operation is `POST /templates` (base URL `https://api.postgrid.com/print-mail/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-template.md) for the provider-specific parameters and requirements.

