# Figma: List Webhooks

Retrieves webhooks from Figma.

```
GET https://connect.mindcloud.co/v1/universal/figma/latest/actions/list-webhooks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Figma `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/figma/latest/actions/list-webhooks?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/figma/latest/actions/list-webhooks?${params}`, {
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
| `context` | list | no | Filter by context type: team, project, or file. |
| `context_id` | string | no | Context identifier to filter webhook results. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `plan_api_id` | string | no | Plan identifier to list webhooks across accessible contexts. |
| `cursor` | string | no | Pagination cursor when listing by plan_api_id. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "clientId": "string",
      "context": "string",
      "contextId": "string",
      "description": "string",
      "endpoint": "string",
      "eventType": "string",
      "id": "string",
      "passcode": "string",
      "planApiId": "string",
      "status": "string",
      "teamId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `clientId` | string |  |
| `context` | string |  |
| `contextId` | string |  |
| `description` | string |  |
| `endpoint` | string |  |
| `eventType` | string |  |
| `id` | string |  |
| `passcode` | string |  |
| `planApiId` | string |  |
| `status` | string |  |
| `teamId` | string |  |

## Native endpoint

Through the native Figma API, this operation is `GET https://api.figma.com/v2/webhooks` (base URL `https://api.figma.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-webhooks.md) for the provider-specific parameters and requirements.

