# Campaign Monitor: List Templates

Retrieves templates for a Campaign Monitor client.

```
GET https://connect.mindcloud.co/v1/universal/campaignMonitor/latest/actions/list-templates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Campaign Monitor `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/campaignMonitor/latest/actions/list-templates?connectionId=$CONNECTION_ID&clientId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "clientId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/campaignMonitor/latest/actions/list-templates?${params}`, {
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
| `clientId` | string | yes | Campaign Monitor client identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "name": "Ava Chen",
      "previewUrl": "https://example.com",
      "screenshotUrl": "https://example.com",
      "templateId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `name` | string | Template name. |
| `previewUrl` | string | Template HTML preview URL. |
| `screenshotUrl` | string | Template screenshot URL. |
| `templateId` | string | Campaign Monitor template identifier. |

## Native endpoint

Through the native Campaign Monitor API, this operation is `GET /clients/:clientId/templates.json` (base URL `https://api.createsend.com/api/v3.3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-templates.md) for the provider-specific parameters and requirements.

