# xMatters: Get devices

Retrieves devices from your xMatters instance.

```
GET https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/get-devices
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a xMatters `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/get-devices?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/get-devices?${params}`, {
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

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "data": [
        {
          "country": "string",
          "defaultDevice": true,
          "delay": 1,
          "description": "string",
          "deviceType": "string",
          "externallyOwned": true,
          "id": "string",
          "links": {
            "next": "https://example.com",
            "self": "https://example.com"
          },
          "list": "string",
          "name": "Ava Chen",
          "owner": {
            "firstName": "Ava",
            "id": "string",
            "lastName": "Chen",
            "links": {
              "self": "https://example.com"
            },
            "recipientType": "string",
            "targetName": "Ava Chen"
          },
          "phoneNumber": "string",
          "priorityThreshold": "string",
          "provider": {
            "id": "string"
          },
          "recipientType": "string",
          "sequence": 1,
          "status": "string",
          "targetName": "Ava Chen",
          "testStatus": "string"
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
| `data[].country` | string |  |
| `data[].defaultDevice` | boolean |  |
| `data[].delay` | number |  |
| `data[].description` | string |  |
| `data[].deviceType` | string |  |
| `data[].externallyOwned` | boolean |  |
| `data[].id` | string |  |
| `data[].links.next` | string |  |
| `data[].links.self` | string |  |
| `data[].list` | string |  |
| `data[].name` | string |  |
| `data[].owner.firstName` | string |  |
| `data[].owner.id` | string |  |
| `data[].owner.lastName` | string |  |
| `data[].owner.links.self` | string |  |
| `data[].owner.recipientType` | string |  |
| `data[].owner.targetName` | string |  |
| `data[].phoneNumber` | string |  |
| `data[].priorityThreshold` | string |  |
| `data[].provider.id` | string |  |
| `data[].recipientType` | string |  |
| `data[].sequence` | number |  |
| `data[].status` | string |  |
| `data[].targetName` | string |  |
| `data[].testStatus` | string |  |
| `total` | number |  |

## Native endpoint

Through the native xMatters API, this operation is `GET devices` (base URL `https://mindcloud.xmatters.com/api/xm/1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-devices.md) for the provider-specific parameters and requirements.

