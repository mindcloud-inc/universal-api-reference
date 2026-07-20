# xMatters: Create a group

Creates a group in your xMatters instance.

```
POST https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/create-a-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a xMatters `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/create-a-group" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/create-a-group', {
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

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `allowDuplicates` | boolean | no |  |
| `description` | string | no |  |
| `observedByAll` | boolean | no |  |
| `observers` | list<string> | no |  |
| `recipientType` | string | no |  |
| `site` | string | no |  |
| `status` | string | no |  |
| `supervisors` | list<string> | no |  |
| `targetName` | string | no |  |
| `useDefaultDevices` | boolean | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "allowDuplicates": true,
      "created": "2026-05-07T12:00:00.000Z",
      "criteria": {
        "criterion": {
          "count": 1,
          "data": [
            {
              "criterionType": "string",
              "field": "string",
              "operand": "string",
              "value": "string"
            }
          ],
          "total": 1
        },
        "operand": "string"
      },
      "description": "string",
      "externallyOwned": true,
      "groupType": "string",
      "id": "string",
      "links": {
        "self": "https://example.com"
      },
      "observedByAll": true,
      "observers": "string",
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
| `created` | date |  |
| `criteria.criterion.count` | number |  |
| `criteria.criterion.data[].criterionType` | string |  |
| `criteria.criterion.data[].field` | string |  |
| `criteria.criterion.data[].operand` | string |  |
| `criteria.criterion.data[].value` | string |  |
| `criteria.criterion.total` | number |  |
| `criteria.operand` | string |  |
| `description` | string |  |
| `externallyOwned` | boolean |  |
| `groupType` | string |  |
| `id` | string |  |
| `links.self` | string |  |
| `observedByAll` | boolean |  |
| `observers` | string |  |
| `recipientType` | string |  |
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
| `supervisors.data[].licenseType` | string |  |
| `supervisors.data[].links.self` | string |  |
| `supervisors.data[].recipientType` | string |  |
| `supervisors.data[].site.id` | string |  |
| `supervisors.data[].site.links.self` | string |  |
| `supervisors.data[].site.name` | string |  |
| `supervisors.data[].status` | string |  |
| `supervisors.data[].targetName` | string |  |
| `supervisors.data[].timezone` | string |  |
| `supervisors.data[].webLogin` | string |  |
| `supervisors.data[].whenCreated` | date |  |
| `supervisors.data[].whenUpdated` | date |  |
| `supervisors.total` | number |  |
| `targetName` | string |  |
| `useDefaultDevices` | boolean |  |

## Native endpoint

Through the native xMatters API, this operation is `POST groups` (base URL `https://mindcloud.xmatters.com/api/xm/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-a-group.md) for the provider-specific parameters and requirements.

