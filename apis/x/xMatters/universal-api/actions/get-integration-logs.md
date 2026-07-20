# xMatters: Get integration logs

Retrieves integration logs from your xMatters instance.

```
GET https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/get-integration-logs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a xMatters `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/get-integration-logs?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/get-integration-logs?${params}`, {
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
| `integrationId` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "data": [
        {
          "by": {
            "firstName": "Ava",
            "id": "string",
            "lastName": "Chen",
            "recipientType": "string",
            "targetName": "Ava Chen"
          },
          "completed": "2026-05-07T12:00:00.000Z",
          "id": "string",
          "integration": {
            "id": "string",
            "links": {
              "self": "https://example.com"
            },
            "name": "Ava Chen",
            "plan": {
              "id": "string",
              "links": {
                "self": "https://example.com"
              }
            }
          },
          "remoteAddress": "string",
          "requestHeaders": {
            "request": "string",
            "requestId": "string",
            "requestMethod": "string",
            "requestParameters": {
              "request": "string",
              "status": "string",
              "url": "https://example.com"
            }
          }
        }
      ],
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
| `data[].by.firstName` | string |  |
| `data[].by.id` | string |  |
| `data[].by.lastName` | string |  |
| `data[].by.recipientType` | string |  |
| `data[].by.targetName` | string |  |
| `data[].completed` | date |  |
| `data[].id` | string |  |
| `data[].integration.id` | string |  |
| `data[].integration.links.self` | string |  |
| `data[].integration.name` | string |  |
| `data[].integration.plan.id` | string |  |
| `data[].integration.plan.links.self` | string |  |
| `data[].remoteAddress` | string |  |
| `data[].requestHeaders.request` | string |  |
| `data[].requestHeaders.requestId` | string |  |
| `data[].requestHeaders.requestMethod` | string |  |
| `data[].requestHeaders.requestParameters.request` | string |  |
| `data[].requestHeaders.requestParameters.status` | string |  |
| `data[].requestHeaders.requestParameters.url` | string |  |
| `total` | number |  |

## Native endpoint

Through the native xMatters API, this operation is `GET integrations/{integrationId}/logs` (base URL `https://mindcloud.xmatters.com/api/xm/1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-integration-logs.md) for the provider-specific parameters and requirements.

