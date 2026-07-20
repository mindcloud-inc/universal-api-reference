# xMatters: Get a person (by id)

Retrieves a person by ID from your xMatters instance.

```
GET https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/get-a-person-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a xMatters `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/get-a-person-by-id?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/get-a-person-by-id?${params}`, {
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
      "lastLogin": "2026-05-07T12:00:00.000Z",
      "lastName": "Chen",
      "licenseType": "string",
      "links": {
        "self": "https://example.com"
      },
      "recipientType": "string",
      "roles": {
        "count": 1,
        "data": [
          {
            "description": "string",
            "id": "string",
            "name": "Ava Chen"
          }
        ],
        "total": 1
      },
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
      "webLogin": "string",
      "whenCreated": "2026-05-07T12:00:00.000Z",
      "whenUpdated": "2026-05-07T12:00:00.000Z"
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
| `lastLogin` | date |  |
| `lastName` | string |  |
| `licenseType` | string |  |
| `links.self` | string |  |
| `recipientType` | string |  |
| `roles.count` | number |  |
| `roles.data[].description` | string |  |
| `roles.data[].id` | string |  |
| `roles.data[].name` | string |  |
| `roles.total` | number |  |
| `site.id` | string |  |
| `site.links.self` | string |  |
| `site.name` | string |  |
| `status` | string |  |
| `targetName` | string |  |
| `timezone` | string |  |
| `webLogin` | string |  |
| `whenCreated` | date |  |
| `whenUpdated` | date |  |

## Native endpoint

Through the native xMatters API, this operation is `GET people/{personId}` (base URL `https://mindcloud.xmatters.com/api/xm/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-a-person-by-id.md) for the provider-specific parameters and requirements.

