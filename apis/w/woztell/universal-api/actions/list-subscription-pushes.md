# Woztell: List Subscription Pushes

Retrieves subscription pushes from your Woztell workspace.

```
GET https://connect.mindcloud.co/v1/universal/woztell/latest/actions/list-subscription-pushes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Woztell `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/woztell/latest/actions/list-subscription-pushes?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/woztell/latest/actions/list-subscription-pushes?${params}`, {
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
| `variables` | object | no | Optional GraphQL variables object. Supported keys include first, after, before, subscriptionPushIds, search, and sortBy. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "apiViewer": {
          "subscriptionPushes": {
            "edges": [
              {
                "node": {
                  "_id": "string",
                  "appId": "string",
                  "createdAt": 1,
                  "description": "string",
                  "etag": "string",
                  "id": "string",
                  "memberCount": 1,
                  "name": "Ava Chen",
                  "priority": 1,
                  "readCount": 1,
                  "scheduleAt": 1,
                  "sentCount": 1,
                  "updatedAt": 1
                }
              }
            ],
            "pageInfo": {
              "endCursor": "string",
              "hasNextPage": true,
              "hasPreviousPage": true,
              "startCursor": "string"
            }
          }
        }
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.apiViewer.subscriptionPushes.edges[].node._id` | string |  |
| `data.apiViewer.subscriptionPushes.edges[].node.appId` | string |  |
| `data.apiViewer.subscriptionPushes.edges[].node.createdAt` | number |  |
| `data.apiViewer.subscriptionPushes.edges[].node.description` | string |  |
| `data.apiViewer.subscriptionPushes.edges[].node.etag` | string |  |
| `data.apiViewer.subscriptionPushes.edges[].node.id` | string |  |
| `data.apiViewer.subscriptionPushes.edges[].node.memberCount` | number |  |
| `data.apiViewer.subscriptionPushes.edges[].node.name` | string |  |
| `data.apiViewer.subscriptionPushes.edges[].node.priority` | number |  |
| `data.apiViewer.subscriptionPushes.edges[].node.readCount` | number |  |
| `data.apiViewer.subscriptionPushes.edges[].node.scheduleAt` | number |  |
| `data.apiViewer.subscriptionPushes.edges[].node.sentCount` | number |  |
| `data.apiViewer.subscriptionPushes.edges[].node.updatedAt` | number |  |
| `data.apiViewer.subscriptionPushes.pageInfo.endCursor` | string |  |
| `data.apiViewer.subscriptionPushes.pageInfo.hasNextPage` | boolean |  |
| `data.apiViewer.subscriptionPushes.pageInfo.hasPreviousPage` | boolean |  |
| `data.apiViewer.subscriptionPushes.pageInfo.startCursor` | string |  |

## Native endpoint

Through the native Woztell API, this operation is `POST /` (base URL `https://open.api.woztell.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-subscription-pushes.md) for the provider-specific parameters and requirements.

