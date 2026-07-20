# Middesk: Retrieve a signal

Retrieves a signal from your Middesk account.

```
GET https://connect.mindcloud.co/v1/universal/middesk/latest/actions/get-signal
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Middesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/middesk/latest/actions/get-signal?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/middesk/latest/actions/get-signal?${params}`, {
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
| `id` | string | yes | ID of the signal to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "addresses": [
        "string"
      ],
      "batchId": "string",
      "businessId": "string",
      "createdAt": "string",
      "externalId": "string",
      "id": "string",
      "modelSlug": "string",
      "name": "Ava Chen",
      "object": "string",
      "people": [
        "string"
      ],
      "reasons": [
        {}
      ],
      "requester": {},
      "score": 1,
      "tin": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `addresses` | array<string> |  |
| `batchId` | string |  |
| `businessId` | string |  |
| `createdAt` | string |  |
| `externalId` | string |  |
| `id` | string |  |
| `modelSlug` | string |  |
| `name` | string |  |
| `object` | string |  |
| `people` | array<string> |  |
| `reasons` | array<object> |  |
| `requester` | object |  |
| `score` | number |  |
| `tin` | string |  |

## Native endpoint

Through the native Middesk API, this operation is `GET /signals/:id` (base URL `https://api.middesk.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-signal.md) for the provider-specific parameters and requirements.

