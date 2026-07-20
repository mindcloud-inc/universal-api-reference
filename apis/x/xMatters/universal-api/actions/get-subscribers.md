# xMatters: Get subscribers

Retrieves subscribers from your xMatters instance.

```
GET https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/get-subscribers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a xMatters `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/get-subscribers?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/get-subscribers?${params}`, {
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
| `subscriptionId` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "data": [
        {
          "externallyOwned": true,
          "firstName": "Ava",
          "id": "string",
          "language": "string",
          "lastLogin": "2026-05-07T12:00:00.000Z",
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
          "targeted": true,
          "targetName": "Ava Chen",
          "timezone": "string",
          "webLogin": "string"
        }
      ],
      "links": {
        "self": "https://example.com"
      },
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number |  |
| `data[].externallyOwned` | boolean |  |
| `data[].firstName` | string |  |
| `data[].id` | string |  |
| `data[].language` | string |  |
| `data[].lastLogin` | date |  |
| `data[].lastName` | string |  |
| `data[].links.self` | string |  |
| `data[].recipientType` | string |  |
| `data[].site.id` | string |  |
| `data[].site.links.self` | string |  |
| `data[].site.name` | string |  |
| `data[].status` | string |  |
| `data[].targeted` | boolean |  |
| `data[].targetName` | string |  |
| `data[].timezone` | string |  |
| `data[].webLogin` | string |  |
| `links.self` | string |  |
| `total` | number |  |

## Native endpoint

Through the native xMatters API, this operation is `GET subscriptions/{subscriptionId}/subscribers` (base URL `https://mindcloud.xmatters.com/api/xm/1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-subscribers.md) for the provider-specific parameters and requirements.

