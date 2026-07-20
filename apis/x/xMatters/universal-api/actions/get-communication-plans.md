# xMatters: Get communication plans

Retrieves communication plans from your xMatters instance.

```
GET https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/get-communication-plans
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a xMatters `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/get-communication-plans?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/get-communication-plans?${params}`, {
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
| `embed` | string | no |  |
| `planType` | string | no |  |
| `search` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
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
          "description": "string",
          "editable": true,
          "enabled": true,
          "floodControl": true,
          "id": "string",
          "links": {
            "self": "https://example.com"
          },
          "loggingLevel": "string",
          "name": "Ava Chen",
          "planType": "string",
          "position": 1
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
| `data[].accessibleByAll` | boolean |  |
| `data[].created` | date |  |
| `data[].creator.externallyOwned` | boolean |  |
| `data[].creator.firstName` | string |  |
| `data[].creator.id` | string |  |
| `data[].creator.language` | string |  |
| `data[].creator.lastName` | string |  |
| `data[].creator.links.self` | string |  |
| `data[].creator.recipientType` | string |  |
| `data[].creator.site.id` | string |  |
| `data[].creator.site.links.self` | string |  |
| `data[].creator.site.name` | string |  |
| `data[].creator.status` | string |  |
| `data[].creator.targetName` | string |  |
| `data[].creator.timezone` | string |  |
| `data[].creator.webLogin` | string |  |
| `data[].description` | string |  |
| `data[].editable` | boolean |  |
| `data[].enabled` | boolean |  |
| `data[].floodControl` | boolean |  |
| `data[].id` | string |  |
| `data[].links.self` | string |  |
| `data[].loggingLevel` | string |  |
| `data[].name` | string |  |
| `data[].planType` | string |  |
| `data[].position` | number |  |
| `links.self` | string |  |
| `total` | number |  |

## Native endpoint

Through the native xMatters API, this operation is `GET plans` (base URL `https://mindcloud.xmatters.com/api/xm/1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-communication-plans.md) for the provider-specific parameters and requirements.

