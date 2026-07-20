# QStash: Get URL Group

Retrieves a URL Group from QStash by name.

```
GET https://connect.mindcloud.co/v1/universal/qStash/latest/actions/get-url-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a QStash `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/qStash/latest/actions/get-url-group?connectionId=$CONNECTION_ID&urlGroupName=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "urlGroupName": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/qStash/latest/actions/get-url-group?${params}`, {
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
| `urlGroupName` | string | yes | Name of the URL Group to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": 1,
      "endpoints": [
        {}
      ],
      "forwardAllHeaders": true,
      "method": "string",
      "name": "Ava Chen",
      "retries": 1,
      "updatedAt": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | number |  |
| `endpoints` | array<object> |  |
| `forwardAllHeaders` | boolean |  |
| `method` | string |  |
| `name` | string |  |
| `retries` | number |  |
| `updatedAt` | number |  |

## Native endpoint

Through the native QStash API, this operation is `GET /v2/topics/:urlGroupName` (base URL `https://qstash-eu-central-1.upstash.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-url-group.md) for the provider-specific parameters and requirements.

