# 1Shot: Search Contract Event Logs

Finds contract event logs in 1Shot API.

```
GET https://connect.mindcloud.co/v1/universal/oneShot/latest/actions/search-contract-event-logs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 1Shot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oneShot/latest/actions/search-contract-event-logs?connectionId=$CONNECTION_ID&contractEventId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "contractEventId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oneShot/latest/actions/search-contract-event-logs?${params}`, {
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
| `contractEventId` | string | yes |  |
| `startBlock` | number | no |  |
| `endBlock` | number | no |  |
| `topics` | list<string> | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "endBlock": 1,
      "error": "string",
      "logs": [
        {
          "blockNumber": 1,
          "blockTimestamp": 1,
          "eventName": "Ava Chen",
          "logIndex": 1,
          "removed": true,
          "topics": {
            "from": "string",
            "to": "string",
            "value": "string"
          },
          "transactionHash": "string"
        }
      ],
      "maxResults": 1,
      "startBlock": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `endBlock` | number |  |
| `error` | string |  |
| `logs[].blockNumber` | number |  |
| `logs[].blockTimestamp` | number |  |
| `logs[].eventName` | string |  |
| `logs[].logIndex` | number |  |
| `logs[].removed` | boolean |  |
| `logs[].topics.from` | string |  |
| `logs[].topics.to` | string |  |
| `logs[].topics.value` | string |  |
| `logs[].transactionHash` | string |  |
| `maxResults` | number |  |
| `startBlock` | number |  |

## Native endpoint

Through the native 1Shot API, this operation is `POST /events/:contractEventId/search` (base URL `https://api.1shotapi.com/v0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-contract-event-logs.md) for the provider-specific parameters and requirements.

