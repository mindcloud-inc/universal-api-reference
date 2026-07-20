# xMatters: Get a group

Retrieves a group from your xMatters instance.

```
GET https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/get-a-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a xMatters `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/get-a-group?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/get-a-group?${params}`, {
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
| `groupId` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "allowDuplicates": true,
      "description": "string",
      "externallyOwned": true,
      "id": "string",
      "links": {
        "self": "https://example.com"
      },
      "observedByAll": true,
      "recipientType": "string",
      "services": {
        "count": 1,
        "data": [
          {
            "description": "string",
            "externallyOwned": true,
            "id": "string",
            "links": {
              "self": "https://example.com"
            },
            "ownedBy": {
              "groupType": "string",
              "id": "string",
              "links": {
                "self": "https://example.com"
              },
              "recipientType": "string",
              "targetName": "Ava Chen"
            },
            "recipientType": "string",
            "status": "string",
            "targetName": "Ava Chen"
          }
        ],
        "total": 1
      },
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
            "externallyOwned": true,
            "firstName": "Ava",
            "id": "string",
            "language": "string",
            "lastLogin": "2026-05-07T12:00:00.000Z",
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
              },
              "name": "Ava Chen"
            },
            "status": "string",
            "targetName": "Ava Chen",
            "timezone": "string",
            "webLogin": "string"
          }
        ],
        "total": 1
      },
      "targetName": "Ava Chen",
      "useDefaultDevices": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `allowDuplicates` | boolean |  |
| `description` | string |  |
| `externallyOwned` | boolean |  |
| `id` | string |  |
| `links.self` | string |  |
| `observedByAll` | boolean |  |
| `recipientType` | string |  |
| `services.count` | number |  |
| `services.data[].description` | string |  |
| `services.data[].externallyOwned` | boolean |  |
| `services.data[].id` | string |  |
| `services.data[].links.self` | string |  |
| `services.data[].ownedBy.groupType` | string |  |
| `services.data[].ownedBy.id` | string |  |
| `services.data[].ownedBy.links.self` | string |  |
| `services.data[].ownedBy.recipientType` | string |  |
| `services.data[].ownedBy.targetName` | string |  |
| `services.data[].recipientType` | string |  |
| `services.data[].status` | string |  |
| `services.data[].targetName` | string |  |
| `services.total` | number |  |
| `site.id` | string |  |
| `site.links.self` | string |  |
| `status` | string |  |
| `supervisors.count` | number |  |
| `supervisors.data[].externallyOwned` | boolean |  |
| `supervisors.data[].firstName` | string |  |
| `supervisors.data[].id` | string |  |
| `supervisors.data[].language` | string |  |
| `supervisors.data[].lastLogin` | date |  |
| `supervisors.data[].lastName` | string |  |
| `supervisors.data[].links.self` | string |  |
| `supervisors.data[].phoneLogin` | string |  |
| `supervisors.data[].recipientType` | string |  |
| `supervisors.data[].site.id` | string |  |
| `supervisors.data[].site.links.self` | string |  |
| `supervisors.data[].site.name` | string |  |
| `supervisors.data[].status` | string |  |
| `supervisors.data[].targetName` | string |  |
| `supervisors.data[].timezone` | string |  |
| `supervisors.data[].webLogin` | string |  |
| `supervisors.total` | number |  |
| `targetName` | string |  |
| `useDefaultDevices` | boolean |  |

## Native endpoint

Through the native xMatters API, this operation is `GET groups/{groupId}` (base URL `https://mindcloud.xmatters.com/api/xm/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-a-group.md) for the provider-specific parameters and requirements.

