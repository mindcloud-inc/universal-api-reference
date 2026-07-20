# Teletype App: Get Project API Status

Retrieves project API status from Teletype App.

```
GET https://connect.mindcloud.co/v1/universal/teletypeApp/latest/actions/get-project-api-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Teletype App `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/teletypeApp/latest/actions/get-project-api-status?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/teletypeApp/latest/actions/get-project-api-status?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "activeWebhooks": [
        "string"
      ],
      "projectId": "string",
      "webhookErrorsCount": 1,
      "webhookUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `activeWebhooks` | array<string> |  |
| `projectId` | string |  |
| `webhookErrorsCount` | number |  |
| `webhookUrl` | string |  |

## Native endpoint

Through the native Teletype App API, this operation is `GET /project/api-status` (base URL `https://api.teletype.app/public/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-project-api-status.md) for the provider-specific parameters and requirements.

