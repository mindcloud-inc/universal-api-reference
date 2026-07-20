# Clio Grow: Create Custom Action



```
POST https://connect.mindcloud.co/v1/universal/clioGrow/latest/actions/create-custom-action
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clio Grow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/clioGrow/latest/actions/create-custom-action" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "label": "string",
  "targetUrl": "https://example.com",
  "uiReference": "matters/show"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/clioGrow/latest/actions/create-custom-action', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "label": "string",
    "targetUrl": "https://example.com",
    "uiReference": "matters/show"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `label` | string | yes | The label of the custom action. |
| `targetUrl` | string | yes | The target HTTPS URL of the custom action. |
| `uiReference` | string | yes | The UI reference for the custom action. Clio currently supports matters/show. One of: `0`. Default: `matters/show`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "label": "string",
      "targetUrl": "https://example.com",
      "uiReference": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `id` | number |  |
| `label` | string |  |
| `targetUrl` | string |  |
| `uiReference` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Clio Grow API, this operation is `POST /custom_actions` (base URL `https://api.clio.com/grow`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-custom-action.md) for the provider-specific parameters and requirements.

