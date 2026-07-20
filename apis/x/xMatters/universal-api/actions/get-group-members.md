# xMatters: Get group members

Retrieves group members from your xMatters instance.

```
GET https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/get-group-members
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a xMatters `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/get-group-members?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/get-group-members?${params}`, {
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
| `groupId` | string | no |  |

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
            "groupType": "string",
            "id": "string",
            "links": {
              "self": "https://example.com"
            },
            "recipientType": "string",
            "targetName": "Ava Chen"
          },
          "member": {
            "firstName": "Ava",
            "id": "string",
            "lastName": "Chen",
            "licenseType": "string",
            "links": {
              "self": "https://example.com"
            },
            "recipientType": "string",
            "targetName": "Ava Chen"
          },
          "shifts": {
            "count": 1,
            "data": [
              {
                "group": {
                  "id": "string",
                  "links": {
                    "self": "https://example.com"
                  }
                },
                "id": "string",
                "links": {
                  "self": "https://example.com"
                },
                "name": "Ava Chen"
              }
            ],
            "total": 1
          }
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
| `data[].group.groupType` | string |  |
| `data[].group.id` | string |  |
| `data[].group.links.self` | string |  |
| `data[].group.recipientType` | string |  |
| `data[].group.targetName` | string |  |
| `data[].member.firstName` | string |  |
| `data[].member.id` | string |  |
| `data[].member.lastName` | string |  |
| `data[].member.licenseType` | string |  |
| `data[].member.links.self` | string |  |
| `data[].member.recipientType` | string |  |
| `data[].member.targetName` | string |  |
| `data[].shifts.count` | number |  |
| `data[].shifts.data[].group.id` | string |  |
| `data[].shifts.data[].group.links.self` | string |  |
| `data[].shifts.data[].id` | string |  |
| `data[].shifts.data[].links.self` | string |  |
| `data[].shifts.data[].name` | string |  |
| `data[].shifts.total` | number |  |
| `links.self` | string |  |
| `total` | number |  |

## Native endpoint

Through the native xMatters API, this operation is `GET groups/{groupId}/members` (base URL `https://mindcloud.xmatters.com/api/xm/1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-group-members.md) for the provider-specific parameters and requirements.

