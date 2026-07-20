# Mendato: List Time Records



```
GET https://connect.mindcloud.co/v1/universal/mendato/latest/actions/list-time-records
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mendato `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mendato/latest/actions/list-time-records?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mendato/latest/actions/list-time-records?${params}`, {
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
| `variables` | object | no | GraphQL variables object for the Mendato time records query. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "timeRecords": {
        "edges": [
          {
            "node": {
              "actualDuration": 1,
              "breakDuration": 1,
              "confirmedAt": "2026-05-07T12:00:00.000Z",
              "createdAt": "2026-05-07T12:00:00.000Z",
              "createdAutomatically": true,
              "date": "2026-05-07T12:00:00.000Z",
              "end": "2026-05-07T12:00:00.000Z",
              "hasTotalBreakInput": true,
              "id": "string",
              "journeyDuration": 1,
              "journeyStart": "2026-05-07T12:00:00.000Z",
              "planDuration": 1,
              "start": "2026-05-07T12:00:00.000Z"
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
| `timeRecords.edges[].node.actualDuration` | number |  |
| `timeRecords.edges[].node.breakDuration` | number |  |
| `timeRecords.edges[].node.confirmedAt` | date |  |
| `timeRecords.edges[].node.createdAt` | date |  |
| `timeRecords.edges[].node.createdAutomatically` | boolean |  |
| `timeRecords.edges[].node.date` | date |  |
| `timeRecords.edges[].node.end` | date |  |
| `timeRecords.edges[].node.hasTotalBreakInput` | boolean |  |
| `timeRecords.edges[].node.id` | string |  |
| `timeRecords.edges[].node.journeyDuration` | number |  |
| `timeRecords.edges[].node.journeyStart` | date |  |
| `timeRecords.edges[].node.planDuration` | number |  |
| `timeRecords.edges[].node.start` | date |  |
| `timeRecords.pageInfo.endCursor` | string |  |
| `timeRecords.pageInfo.hasNextPage` | boolean |  |
| `timeRecords.pageInfo.hasPreviousPage` | boolean |  |
| `timeRecords.pageInfo.startCursor` | string |  |
| `timeRecords.totalCount` | number |  |

## Native endpoint

Through the native Mendato API, this operation is `POST /graphql` (base URL `https://api.mendato.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-time-records.md) for the provider-specific parameters and requirements.

