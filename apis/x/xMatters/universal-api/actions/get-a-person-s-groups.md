# xMatters: Get a person's groups

Retrieves a person's groups from your xMatters instance.

```
GET https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/get-a-person-s-groups
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a xMatters `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/get-a-person-s-groups?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/get-a-person-s-groups?${params}`, {
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
      "count": 1,
      "data": [
        {
          "group": {
            "id": "string",
            "links": {
              "self": "https://example.com"
            },
            "recipientType": "string",
            "targetName": "Ava Chen"
          },
          "links": {
            "self": "https://example.com"
          },
          "member": {
            "firstName": "Ava",
            "id": "string",
            "lastName": "Chen",
            "links": {
              "self": "https://example.com"
            },
            "recipientType": "string",
            "targetName": "Ava Chen"
          }
        }
      ],
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
| `data[].group.id` | string |  |
| `data[].group.links.self` | string |  |
| `data[].group.recipientType` | string |  |
| `data[].group.targetName` | string |  |
| `data[].links.self` | string |  |
| `data[].member.firstName` | string |  |
| `data[].member.id` | string |  |
| `data[].member.lastName` | string |  |
| `data[].member.links.self` | string |  |
| `data[].member.recipientType` | string |  |
| `data[].member.targetName` | string |  |
| `total` | number |  |

## Native endpoint

Through the native xMatters API, this operation is `GET people/{personId}/group-memberships` (base URL `https://mindcloud.xmatters.com/api/xm/1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-a-person-s-groups.md) for the provider-specific parameters and requirements.

