# Swipe One: List Segments



```
GET https://connect.mindcloud.co/v1/universal/swipeOne/latest/actions/list-segments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Swipe One `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/swipeOne/latest/actions/list-segments?connectionId=$CONNECTION_ID&workspaceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workspaceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/swipeOne/latest/actions/list-segments?${params}`, {
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
| `workspaceId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "count": 1,
        "segments": [
          {
            "contactCount": 1,
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
        ]
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
| `data.count` | number |  |
| `data.segments[].contactCount` | number |  |
| `data.segments[].createdAt` | string |  |
| `data.segments[].createdBy.id` | string |  |
| `data.segments[].createdBy.name` | string |  |
| `data.segments[].createdBy.type` | string |  |
| `data.segments[].criteria.predicates[].dataType` | string |  |
| `data.segments[].criteria.predicates[].operator` | string |  |
| `data.segments[].criteria.predicates[].property` | string |  |
| `data.segments[].criteria.predicates[].value[]` | string |  |
| `data.segments[].criteria.type` | string |  |
| `data.segments[].Id` | string |  |
| `data.segments[].name` | string |  |
| `data.segments[].updatedAt` | string |  |
| `data.segments[].V` | number |  |
| `data.segments[].workspaceId` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Swipe One API, this operation is `GET /workspaces/:workspaceId/segments` (base URL `https://api.swipeone.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-segments.md) for the provider-specific parameters and requirements.

