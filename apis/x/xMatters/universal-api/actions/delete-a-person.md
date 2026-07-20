# xMatters: Delete a person

Deletes a person from your xMatters instance.

```
DELETE https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/delete-a-person
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a xMatters `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/delete-a-person?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/delete-a-person?${params}`, {
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
| `personId` | string | no |  |

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

Through the native xMatters API, this operation is `DELETE people/{personId}` (base URL `https://mindcloud.xmatters.com/api/xm/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-a-person.md) for the provider-specific parameters and requirements.

