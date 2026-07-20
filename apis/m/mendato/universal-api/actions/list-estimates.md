# Mendato: List Estimates



```
GET https://connect.mindcloud.co/v1/universal/mendato/latest/actions/list-estimates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mendato `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mendato/latest/actions/list-estimates?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mendato/latest/actions/list-estimates?${params}`, {
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
| `variables` | object | no | GraphQL variables object for the Mendato estimates query. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "estimates": {
        "edges": [
          {
            "node": {
              "acceptedAt": "2026-05-07T12:00:00.000Z",
              "completedAt": "2026-05-07T12:00:00.000Z",
              "createdAt": "2026-05-07T12:00:00.000Z",
              "declinedAt": "2026-05-07T12:00:00.000Z",
              "declineReason": "string",
              "estimateDate": "2026-05-07T12:00:00.000Z",
              "hasKleinunternehmerregelung": true,
              "id": "string",
              "isAnsweredByCustomer": true,
              "number": 1,
              "numberPrefix": "string",
              "sentAt": "2026-05-07T12:00:00.000Z",
              "sentManually": true,
              "status": "string",
              "validityDate": "2026-05-07T12:00:00.000Z",
              "webEnabled": true,
              "webUrl": "https://example.com"
            }
          }
        ],
        "pageInfo": {
          "endCursor": "string",
          "hasNextPage": true,
          "hasPreviousPage": true,
          "startCursor": "string"
        },
        "totalCount": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `estimates.edges[].node.acceptedAt` | date |  |
| `estimates.edges[].node.completedAt` | date |  |
| `estimates.edges[].node.createdAt` | date |  |
| `estimates.edges[].node.declinedAt` | date |  |
| `estimates.edges[].node.declineReason` | string |  |
| `estimates.edges[].node.estimateDate` | date |  |
| `estimates.edges[].node.hasKleinunternehmerregelung` | boolean |  |
| `estimates.edges[].node.id` | string |  |
| `estimates.edges[].node.isAnsweredByCustomer` | boolean |  |
| `estimates.edges[].node.number` | number |  |
| `estimates.edges[].node.numberPrefix` | string |  |
| `estimates.edges[].node.sentAt` | date |  |
| `estimates.edges[].node.sentManually` | boolean |  |
| `estimates.edges[].node.status` | string |  |
| `estimates.edges[].node.validityDate` | date |  |
| `estimates.edges[].node.webEnabled` | boolean |  |
| `estimates.edges[].node.webUrl` | string |  |
| `estimates.pageInfo.endCursor` | string |  |
| `estimates.pageInfo.hasNextPage` | boolean |  |
| `estimates.pageInfo.hasPreviousPage` | boolean |  |
| `estimates.pageInfo.startCursor` | string |  |
| `estimates.totalCount` | number |  |

## Native endpoint

Through the native Mendato API, this operation is `POST /graphql` (base URL `https://api.mendato.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-estimates.md) for the provider-specific parameters and requirements.

