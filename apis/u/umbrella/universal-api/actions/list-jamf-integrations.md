# Umbrella: List Jamf Integrations

Retrieves Jamf integration records from Umbrella.

```
GET https://connect.mindcloud.co/v1/universal/umbrella/latest/actions/list-jamf-integrations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Umbrella `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/umbrella/latest/actions/list-jamf-integrations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/umbrella/latest/actions/list-jamf-integrations?${params}`, {
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
      "config": {},
      "createdAt": "2026-05-07T12:00:00.000Z",
      "createdBy": "string",
      "createdFromIp": "string",
      "href": "https://example.com",
      "id": "string",
      "name": "Ava Chen",
      "status": "string",
      "type": "string",
      "webhookConfig": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `config` | object |  |
| `createdAt` | date |  |
| `createdBy` | string |  |
| `createdFromIp` | string |  |
| `href` | string |  |
| `id` | string |  |
| `name` | string |  |
| `status` | string |  |
| `type` | string |  |
| `webhookConfig` | object |  |

## Native endpoint

Through the native Umbrella API, this operation is `GET https://api.sse.cisco.com/admin/v2/integrations?type=jamf.v1` (base URL `https://api.umbrella.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-jamf-integrations.md) for the provider-specific parameters and requirements.

