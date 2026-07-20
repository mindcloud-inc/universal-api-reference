# Swipe One: Create Segment



```
POST https://connect.mindcloud.co/v1/universal/swipeOne/latest/actions/create-segment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Swipe One `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/swipeOne/latest/actions/create-segment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "workspaceId": "string",
  "name": "Ava Chen",
  "copyViewFrom": "string",
  "criteria": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/swipeOne/latest/actions/create-segment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "workspaceId": "string",
    "name": "Ava Chen",
    "copyViewFrom": "string",
    "criteria": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `workspaceId` | string | yes |  |
| `name` | string | yes |  |
| `copyViewFrom` | string | yes | Source segment or view identifier to copy when creating a segment. |
| `criteria` | object | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "segment": {
          "contactPropertiesUsed": [
            "string"
          ],
          "createdAt": "string",
          "createdBy": {
            "id": "string",
            "name": "Ava Chen",
            "type": "string"
          },
          "criteria": {
            "predicates": [
              {
                "dataType": "string",
                "operator": "string",
                "property": "string",
                "value": [
                  "string"
                ]
              }
            ],
            "type": "string"
          },
          "Id": "string",
          "name": "Ava Chen",
          "updatedAt": "string",
          "V": 1,
          "workspaceId": "string"
        }
      },
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.segment.contactPropertiesUsed[]` | string |  |
| `data.segment.createdAt` | string |  |
| `data.segment.createdBy.id` | string |  |
| `data.segment.createdBy.name` | string |  |
| `data.segment.createdBy.type` | string |  |
| `data.segment.criteria.predicates[].dataType` | string |  |
| `data.segment.criteria.predicates[].operator` | string |  |
| `data.segment.criteria.predicates[].property` | string |  |
| `data.segment.criteria.predicates[].value[]` | string |  |
| `data.segment.criteria.type` | string |  |
| `data.segment.Id` | string |  |
| `data.segment.name` | string |  |
| `data.segment.updatedAt` | string |  |
| `data.segment.V` | number |  |
| `data.segment.workspaceId` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Swipe One API, this operation is `POST /workspaces/:workspaceId/segments` (base URL `https://api.swipeone.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-segment.md) for the provider-specific parameters and requirements.

