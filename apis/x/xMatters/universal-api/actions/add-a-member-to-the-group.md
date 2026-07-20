# xMatters: Add a member to the group

Adds a member to the group in your xMatters instance.

```
POST https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/add-a-member-to-the-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a xMatters `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/add-a-member-to-the-group" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/add-a-member-to-the-group', {
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
| `groupId` | string | no |  |
| `id` | string | no |  |
| `recipientType` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
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
        }
      },
      "status": "string",
      "targetName": "Ava Chen",
      "timezone": "string",
      "webLogin": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `externallyOwned` | boolean |  |
| `firstName` | string |  |
| `id` | string |  |
| `language` | string |  |
| `lastName` | string |  |
| `links.self` | string |  |
| `recipientType` | string |  |
| `site.id` | string |  |
| `site.links.self` | string |  |
| `status` | string |  |
| `targetName` | string |  |
| `timezone` | string |  |
| `webLogin` | string |  |

## Native endpoint

Through the native xMatters API, this operation is `POST groups/{groupId}/members` (base URL `https://mindcloud.xmatters.com/api/xm/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-a-member-to-the-group.md) for the provider-specific parameters and requirements.

