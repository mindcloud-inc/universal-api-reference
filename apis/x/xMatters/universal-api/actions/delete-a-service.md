# xMatters: Delete a service

Deletes a service from your xMatters instance.

```
DELETE https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/delete-a-service
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a xMatters `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/delete-a-service?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/delete-a-service?${params}`, {
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
| `serviceId` | string | no |  |

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

Through the native xMatters API, this operation is `DELETE services/{serviceId}` (base URL `https://mindcloud.xmatters.com/api/xm/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-a-service.md) for the provider-specific parameters and requirements.

