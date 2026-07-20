# xMatters: Get incidents

Retrieves incidents from your xMatters instance.

```
GET https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/get-incidents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a xMatters `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/get-incidents?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/get-incidents?${params}`, {
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
          "commander": {
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
          "createdAt": "2026-05-07T12:00:00.000Z",
          "description": "string",
          "id": "string",
          "impactedServices": [
            {
              "description": "string",
              "externallyOwned": true,
              "id": "string",
              "links": {
                "self": "https://example.com"
              },
              "recipientType": "string",
              "status": "string",
              "targetName": "Ava Chen"
            }
          ],
          "incidentIdentifier": "string",
          "initiatedBy": {
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
          "links": {
            "self": "https://example.com"
          },
          "severity": {
            "name": "Ava Chen"
          },
          "status": {
            "name": "Ava Chen"
          },
          "summary": "string",
          "updatedAt": "2026-05-07T12:00:00.000Z"
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
| `data[].commander.firstName` | string |  |
| `data[].commander.id` | string |  |
| `data[].commander.lastName` | string |  |
| `data[].commander.licenseType` | string |  |
| `data[].commander.links.self` | string |  |
| `data[].commander.recipientType` | string |  |
| `data[].commander.targetName` | string |  |
| `data[].createdAt` | date |  |
| `data[].description` | string |  |
| `data[].id` | string |  |
| `data[].impactedServices[].description` | string |  |
| `data[].impactedServices[].externallyOwned` | boolean |  |
| `data[].impactedServices[].id` | string |  |
| `data[].impactedServices[].links.self` | string |  |
| `data[].impactedServices[].recipientType` | string |  |
| `data[].impactedServices[].status` | string |  |
| `data[].impactedServices[].targetName` | string |  |
| `data[].incidentIdentifier` | string |  |
| `data[].initiatedBy.firstName` | string |  |
| `data[].initiatedBy.id` | string |  |
| `data[].initiatedBy.lastName` | string |  |
| `data[].initiatedBy.licenseType` | string |  |
| `data[].initiatedBy.links.self` | string |  |
| `data[].initiatedBy.recipientType` | string |  |
| `data[].initiatedBy.targetName` | string |  |
| `data[].links.self` | string |  |
| `data[].severity.name` | string |  |
| `data[].status.name` | string |  |
| `data[].summary` | string |  |
| `data[].updatedAt` | date |  |
| `links.self` | string |  |
| `total` | number |  |

## Native endpoint

Through the native xMatters API, this operation is `GET incidents` (base URL `https://mindcloud.xmatters.com/api/xm/1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-incidents.md) for the provider-specific parameters and requirements.

