# Alto: Get Negotiator

Retrieves a negotiator from Alto by ID.

```
GET https://connect.mindcloud.co/v1/universal/alto/latest/actions/get-negotiator
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Alto `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/alto/latest/actions/get-negotiator?connectionId=$CONNECTION_ID&negotiatorId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "negotiatorId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/alto/latest/actions/get-negotiator?${params}`, {
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
| `negotiatorId` | string | yes | Unique Alto negotiator identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "authorisedSignatory": true,
      "email": "ava@example.com",
      "id": "string",
      "name": "Ava Chen",
      "phoneNumber": "string",
      "role": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `authorisedSignatory` | boolean |  |
| `email` | string |  |
| `id` | string |  |
| `name` | string |  |
| `phoneNumber` | string |  |
| `role` | string |  |

## Native endpoint

Through the native Alto API, this operation is `GET /negotiators/:negotiatorId` (base URL `https://api.alto.zoopladev.co.uk`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-negotiator.md) for the provider-specific parameters and requirements.

