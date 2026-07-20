# Emelia: Add Webhook To Scrap

Adds a webhook to a scrap in Emelia.

```
PUT https://connect.mindcloud.co/v1/universal/emelia/latest/actions/add-webhook-to-scrap
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Emelia `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/emelia/latest/actions/add-webhook-to-scrap" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "events": "string",
  "id": "string",
  "webhookUrl": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/emelia/latest/actions/add-webhook-to-scrap', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "events": "string",
    "id": "string",
    "webhookUrl": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `events` | string | yes | Webhook event list. Provide a JSON array string, for example ["finished"]. |
| `id` | string | yes | Scrap identifier |
| `webhookUrl` | string | yes | Webhook URL |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "addWebhookToScrap": {}
      },
      "errors": [
        {
          "extensions": {
            "code": "string"
          },
          "locations": [
            {
              "column": 1,
              "line": 1
            }
          ],
          "message": "string",
          "path": [
            "string"
          ]
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.addWebhookToScrap` | object |  |
| `errors[].extensions.code` | string |  |
| `errors[].locations[].column` | number |  |
| `errors[].locations[].line` | number |  |
| `errors[].message` | string |  |
| `errors[].path[]` | string |  |

## Native endpoint

Through the native Emelia API, this operation is `POST /graphql` (base URL `https://graphql.emelia.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-webhook-to-scrap.md) for the provider-specific parameters and requirements.

