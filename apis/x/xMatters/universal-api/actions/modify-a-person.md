# xMatters: Modify a person

Updates a person in your xMatters instance.

```
PUT https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/modify-a-person
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a xMatters `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/modify-a-person" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/modify-a-person', {
  method: 'PUT',
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
| `id` | string | no |  |
| `status` | string | no |  |

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
      "licenseType": "string",
      "links": {
        "self": "https://example.com"
      },
      "phoneLogin": "string",
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
| `licenseType` | string |  |
| `links.self` | string |  |
| `phoneLogin` | string |  |
| `recipientType` | string |  |
| `site.id` | string |  |
| `site.links.self` | string |  |
| `status` | string |  |
| `targetName` | string |  |
| `timezone` | string |  |
| `webLogin` | string |  |

## Native endpoint

Through the native xMatters API, this operation is `POST people` (base URL `https://mindcloud.xmatters.com/api/xm/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/modify-a-person.md) for the provider-specific parameters and requirements.

