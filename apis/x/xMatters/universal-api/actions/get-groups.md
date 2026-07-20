# xMatters: Get groups

Retrieves groups from your xMatters instance.

```
GET https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/get-groups
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a xMatters `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/get-groups?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/get-groups?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "data": [
        {
          "allowDuplicates": true,
          "description": "string",
          "externallyOwned": true,
          "groupType": "string",
          "id": "string",
          "links": {
            "self": "https://example.com"
          },
          "observedByAll": true,
          "observers": {
            "count": 1,
            "data": [
              {
                "id": "string",
                "name": "Ava Chen"
              }
            ],
            "total": 1
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
          "useDefaultDevices": true
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
| `data[].allowDuplicates` | boolean |  |
| `data[].description` | string |  |
| `data[].externallyOwned` | boolean |  |
| `data[].groupType` | string |  |
| `data[].id` | string |  |
| `data[].links.self` | string |  |
| `data[].observedByAll` | boolean |  |
| `data[].observers.count` | number |  |
| `data[].observers.data[].id` | string |  |
| `data[].observers.data[].name` | string |  |
| `data[].observers.total` | number |  |
| `data[].recipientType` | string |  |
| `data[].site.id` | string |  |
| `data[].site.links.self` | string |  |
| `data[].status` | string |  |
| `data[].targetName` | string |  |
| `data[].useDefaultDevices` | boolean |  |
| `links.self` | string |  |
| `total` | number |  |

## Native endpoint

Through the native xMatters API, this operation is `GET groups` (base URL `https://mindcloud.xmatters.com/api/xm/1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-groups.md) for the provider-specific parameters and requirements.

