# xMatters: Update form recipients

Updates form recipients in your xMatters instance.

```
PUT https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/update-form-recipients
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a xMatters `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/update-form-recipients" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/update-form-recipients', {
  method: 'PUT',
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

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `formId` | string | no |  |

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
          "created": "2026-05-07T12:00:00.000Z",
          "description": "string",
          "externallyOwned": true,
          "firstName": "Ava",
          "groupType": "string",
          "id": "string",
          "language": "string",
          "lastLogin": "2026-05-07T12:00:00.000Z",
          "lastName": "Chen",
          "licenseType": "string",
          "links": {
            "self": "https://example.com"
          },
          "observedByAll": true,
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
          "useDefaultDevices": true,
          "webLogin": "string",
          "whenCreated": "2026-05-07T12:00:00.000Z",
          "whenUpdated": "2026-05-07T12:00:00.000Z"
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
| `data[].created` | date |  |
| `data[].description` | string |  |
| `data[].externallyOwned` | boolean |  |
| `data[].firstName` | string |  |
| `data[].groupType` | string |  |
| `data[].id` | string |  |
| `data[].language` | string |  |
| `data[].lastLogin` | date |  |
| `data[].lastName` | string |  |
| `data[].licenseType` | string |  |
| `data[].links.self` | string |  |
| `data[].observedByAll` | boolean |  |
| `data[].recipientType` | string |  |
| `data[].site.id` | string |  |
| `data[].site.links.self` | string |  |
| `data[].site.name` | string |  |
| `data[].status` | string |  |
| `data[].targeted` | boolean |  |
| `data[].targetName` | string |  |
| `data[].timezone` | string |  |
| `data[].useDefaultDevices` | boolean |  |
| `data[].webLogin` | string |  |
| `data[].whenCreated` | date |  |
| `data[].whenUpdated` | date |  |
| `links.self` | string |  |
| `total` | number |  |

## Native endpoint

Through the native xMatters API, this operation is `PUT forms/{formId}/recipients` (base URL `https://mindcloud.xmatters.com/api/xm/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-form-recipients.md) for the provider-specific parameters and requirements.

