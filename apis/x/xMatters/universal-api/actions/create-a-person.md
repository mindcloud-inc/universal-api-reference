# xMatters: Create a person

Creates a person in your xMatters instance.

```
POST https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/create-a-person
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a xMatters `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/create-a-person" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/create-a-person', {
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
      "properties": {
        "myCheckboxCustomField": true,
        "myCustomAttribute": [
          [
            "string"
          ]
        ],
        "myDecimalCustomField": 1,
        "myIntegerCustomField": 1,
        "myListCustomField": "string",
        "myPasswordCustomField": "string",
        "myTextCustomField": "string"
      },
      "recipientType": "string",
      "site": {
        "id": "string",
        "links": {
          "self": "https://example.com"
        }
      },
      "status": "string",
      "supervisors": {
        "count": 1,
        "data": [
          {
            "firstName": "Ava",
            "id": "string",
            "lastName": "Chen",
            "links": {
              "self": "https://example.com"
            },
            "recipientType": "string",
            "status": "string",
            "targetName": "Ava Chen"
          }
        ],
        "links": {
          "self": "https://example.com"
        },
        "total": 1
      },
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
| `properties.myCheckboxCustomField` | boolean |  |
| `properties.myCustomAttribute[]` | array<string> |  |
| `properties.myDecimalCustomField` | number |  |
| `properties.myIntegerCustomField` | number |  |
| `properties.myListCustomField` | string |  |
| `properties.myPasswordCustomField` | string |  |
| `properties.myTextCustomField` | string |  |
| `recipientType` | string |  |
| `site.id` | string |  |
| `site.links.self` | string |  |
| `status` | string |  |
| `supervisors.count` | number |  |
| `supervisors.data[].firstName` | string |  |
| `supervisors.data[].id` | string |  |
| `supervisors.data[].lastName` | string |  |
| `supervisors.data[].links.self` | string |  |
| `supervisors.data[].recipientType` | string |  |
| `supervisors.data[].status` | string |  |
| `supervisors.data[].targetName` | string |  |
| `supervisors.links.self` | string |  |
| `supervisors.total` | number |  |
| `targetName` | string |  |
| `timezone` | string |  |
| `webLogin` | string |  |

## Native endpoint

Through the native xMatters API, this operation is `POST people` (base URL `https://mindcloud.xmatters.com/api/xm/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-a-person.md) for the provider-specific parameters and requirements.

