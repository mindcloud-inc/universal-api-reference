# CoordinateHQ: List Project Group



```
GET https://connect.mindcloud.co/v1/universal/coordinateHQ/latest/actions/list-project-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CoordinateHQ `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/coordinateHQ/latest/actions/list-project-group?connectionId=$CONNECTION_ID&projectId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/coordinateHQ/latest/actions/list-project-group?${params}`, {
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
| `projectId` | string | yes |  |
| `lastModifiedDate` | string | no |  |
| `sort` | list<string> | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "customers": [
        {
          "customerId": "string",
          "customerName": "Ava Chen"
        }
      ],
      "entityType": "string",
      "entityUrl": "https://example.com",
      "groupCompletedDt": {},
      "groupId": "string",
      "groupTargetDate": {},
      "groupTitle": "string",
      "lastModifiedDt": "string",
      "projectId": "string",
      "projectName": "Ava Chen",
      "vendorId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `customers[].customerId` | string |  |
| `customers[].customerName` | string |  |
| `entityType` | string |  |
| `entityUrl` | string |  |
| `groupCompletedDt` | object |  |
| `groupId` | string |  |
| `groupTargetDate` | object |  |
| `groupTitle` | string |  |
| `lastModifiedDt` | string |  |
| `projectId` | string |  |
| `projectName` | string |  |
| `vendorId` | string |  |

## Native endpoint

Through the native CoordinateHQ API, this operation is `GET /projects/:projectId/group` (base URL `https://app.coordinatehq.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-project-group.md) for the provider-specific parameters and requirements.

