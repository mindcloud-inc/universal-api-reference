# DirectIQ: Create Campaign Overview Export

Creates a campaign overview export in DirectIQ.

```
POST https://connect.mindcloud.co/v1/universal/directiq/latest/actions/create-campaign-overview-export
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DirectIQ `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/directiq/latest/actions/create-campaign-overview-export" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/directiq/latest/actions/create-campaign-overview-export', {
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



## Response

```json
{
  "success": true,
  "data": [
    {
      "createdUtcDate": "2026-05-07T12:00:00.000Z",
      "downloadUrl": "https://example.com",
      "name": "Ava Chen",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdUtcDate` | date |  |
| `downloadUrl` | string |  |
| `name` | string |  |
| `status` | string |  |

## Native endpoint

Through the native DirectIQ API, this operation is `POST /core/export/campaignoverview` (base URL `https://rest.directiq.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-campaign-overview-export.md) for the provider-specific parameters and requirements.

