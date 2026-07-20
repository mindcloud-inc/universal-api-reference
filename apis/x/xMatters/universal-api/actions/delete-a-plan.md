# xMatters: Delete a plan

Deletes a plan from your xMatters instance.

```
DELETE https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/delete-a-plan
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a xMatters `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/delete-a-plan?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/delete-a-plan?${params}`, {
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
| `planId` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accessibleByAll": true,
      "created": "2026-05-07T12:00:00.000Z",
      "creator": {
        "externallyOwned": true,
        "firstName": "Ava",
        "id": "string",
        "language": "string",
        "lastName": "Chen",
        "links": {
          "self": "https://example.com"
        },
        "recipientType": "string",
        "site": {
          "id": "string",
          "links": {
            "self": "https://example.com"
          },
          "name": "Ava Chen"
        },
        "status": "string",
        "targetName": "Ava Chen",
        "timezone": "string",
        "webLogin": "string"
      },
      "editable": true,
      "enabled": true,
      "floodControl": true,
      "id": "string",
      "links": {
        "self": "https://example.com"
      },
      "loggingLevel": "string",
      "name": "Ava Chen",
      "planType": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accessibleByAll` | boolean |  |
| `created` | date |  |
| `creator.externallyOwned` | boolean |  |
| `creator.firstName` | string |  |
| `creator.id` | string |  |
| `creator.language` | string |  |
| `creator.lastName` | string |  |
| `creator.links.self` | string |  |
| `creator.recipientType` | string |  |
| `creator.site.id` | string |  |
| `creator.site.links.self` | string |  |
| `creator.site.name` | string |  |
| `creator.status` | string |  |
| `creator.targetName` | string |  |
| `creator.timezone` | string |  |
| `creator.webLogin` | string |  |
| `editable` | boolean |  |
| `enabled` | boolean |  |
| `floodControl` | boolean |  |
| `id` | string |  |
| `links.self` | string |  |
| `loggingLevel` | string |  |
| `name` | string |  |
| `planType` | string |  |

## Native endpoint

Through the native xMatters API, this operation is `DELETE plans/{planId}` (base URL `https://mindcloud.xmatters.com/api/xm/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-a-plan.md) for the provider-specific parameters and requirements.

