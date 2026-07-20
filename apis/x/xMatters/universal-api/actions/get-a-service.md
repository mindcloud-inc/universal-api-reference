# xMatters: Get a service

Retrieves a service from your xMatters instance.

```
GET https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/get-a-service
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a xMatters `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/get-a-service?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/get-a-service?${params}`, {
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
| `serviceId` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "data": [
        {
          "description": "string",
          "id": "string",
          "links": {
            "self": "https://example.com"
          },
          "ownedBy": {
            "id": "string",
            "links": {
              "self": "https://example.com"
            },
            "recipientType": "string",
            "targetName": "Ava Chen"
          },
          "recipientType": "string",
          "serviceTier": "string",
          "serviceType": "string",
          "targetName": "Ava Chen"
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
| `data[].description` | string |  |
| `data[].id` | string |  |
| `data[].links.self` | string |  |
| `data[].ownedBy.id` | string |  |
| `data[].ownedBy.links.self` | string |  |
| `data[].ownedBy.recipientType` | string |  |
| `data[].ownedBy.targetName` | string |  |
| `data[].recipientType` | string |  |
| `data[].serviceTier` | string |  |
| `data[].serviceType` | string |  |
| `data[].targetName` | string |  |
| `total` | number |  |

## Native endpoint

Through the native xMatters API, this operation is `GET services/{serviceId}` (base URL `https://mindcloud.xmatters.com/api/xm/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-a-service.md) for the provider-specific parameters and requirements.

