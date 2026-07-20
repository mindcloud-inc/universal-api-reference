# xMatters: Create a service

Creates a service in your xMatters instance.

```
POST https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/create-a-service
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a xMatters `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/create-a-service" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/create-a-service', {
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
| `description` | string | no |  |
| `ownedBy` | string | no |  |
| `serviceTier` | string | no |  |
| `serviceType` | string | no |  |
| `targetName` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "description": "string",
      "id": "string",
      "links": {
        "self": "https://example.com"
      },
      "ownedBy": {
        "id": "string",
        "links": {
          "self": "https://example.com"
        },
        "recipientType": "string",
        "targetName": "Ava Chen"
      },
      "recipientType": "string",
      "serviceTier": "string",
      "serviceType": "string",
      "targetName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string |  |
| `id` | string |  |
| `links.self` | string |  |
| `ownedBy.id` | string |  |
| `ownedBy.links.self` | string |  |
| `ownedBy.recipientType` | string |  |
| `ownedBy.targetName` | string |  |
| `recipientType` | string |  |
| `serviceTier` | string |  |
| `serviceType` | string |  |
| `targetName` | string |  |

## Native endpoint

Through the native xMatters API, this operation is `POST services` (base URL `https://mindcloud.xmatters.com/api/xm/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-a-service.md) for the provider-specific parameters and requirements.

