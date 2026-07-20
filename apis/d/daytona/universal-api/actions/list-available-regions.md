# Daytona: List Available Regions

Retrieves the available regions from Daytona.

```
GET https://connect.mindcloud.co/v1/universal/daytona/latest/actions/list-available-regions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Daytona `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/daytona/latest/actions/list-available-regions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/daytona/latest/actions/list-available-regions?${params}`, {
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
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "name": "Ava Chen",
      "organizationId": "string",
      "proxyUrl": "https://example.com",
      "regionType": "string",
      "snapshotManagerUrl": "https://example.com",
      "sshGatewayUrl": "https://example.com",
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
| `id` | string |  |
| `name` | string |  |
| `organizationId` | string |  |
| `proxyUrl` | string |  |
| `regionType` | string |  |
| `snapshotManagerUrl` | string |  |
| `sshGatewayUrl` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Daytona API, this operation is `GET /regions` (base URL `https://app.daytona.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-available-regions.md) for the provider-specific parameters and requirements.

