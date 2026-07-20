# 1Shot: Get Contract Event

Retrieves contract event details from 1Shot API.

```
GET https://connect.mindcloud.co/v1/universal/oneShot/latest/actions/get-contract-event
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 1Shot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oneShot/latest/actions/get-contract-event?connectionId=$CONNECTION_ID&contractEventId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "contractEventId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oneShot/latest/actions/get-contract-event?${params}`, {
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
| `contractEventId` | string | yes | The internal UUID of the contract event. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "businessId": "string",
      "chainId": 1,
      "contractAddress": "string",
      "created": 1,
      "description": "string",
      "eventName": "Ava Chen",
      "id": "string",
      "name": "Ava Chen",
      "topicHash": "string",
      "topics": [
        {
          "indexed": true,
          "name": "Ava Chen"
        }
      ],
      "updated": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `businessId` | string |  |
| `chainId` | number |  |
| `contractAddress` | string |  |
| `created` | number |  |
| `description` | string |  |
| `eventName` | string |  |
| `id` | string |  |
| `name` | string |  |
| `topicHash` | string |  |
| `topics[].indexed` | boolean |  |
| `topics[].name` | string |  |
| `updated` | number |  |

## Native endpoint

Through the native 1Shot API, this operation is `GET /events/:contractEventId` (base URL `https://api.1shotapi.com/v0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-contract-event.md) for the provider-specific parameters and requirements.

