# Svix: Get Connector

Retrieves a connector from Svix.

```
GET https://connect.mindcloud.co/v1/universal/svix/latest/actions/get-connector
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Svix `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/svix/latest/actions/get-connector?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/svix/latest/actions/get-connector?${params}`, {
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
      "allowedEventTypes": [
        "string"
      ],
      "createdAt": "string",
      "description": "string",
      "featureFlags": [
        "string"
      ],
      "id": "string",
      "instructions": "string",
      "kind": "string",
      "logo": "string",
      "name": "Ava Chen",
      "orgId": "string",
      "productType": "string",
      "transformation": "string",
      "transformationUpdatedAt": "string",
      "uid": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `allowedEventTypes` | array<string> |  |
| `createdAt` | string |  |
| `description` | string |  |
| `featureFlags` | array<string> |  |
| `id` | string |  |
| `instructions` | string |  |
| `kind` | string |  |
| `logo` | string |  |
| `name` | string |  |
| `orgId` | string |  |
| `productType` | string |  |
| `transformation` | string |  |
| `transformationUpdatedAt` | string |  |
| `uid` | string |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Svix API, this operation is `GET /api/v1/connector/{connector_id}` (base URL `https://api.us.svix.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-connector.md) for the provider-specific parameters and requirements.

