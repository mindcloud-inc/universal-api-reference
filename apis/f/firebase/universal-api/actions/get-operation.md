# Firebase: Get Operation

Retrieves an operation from Firebase.

```
GET https://connect.mindcloud.co/v1/universal/firebase/latest/actions/get-operation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Firebase `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/firebase/latest/actions/get-operation?connectionId=$CONNECTION_ID&operationId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "operationId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/firebase/latest/actions/get-operation?${params}`, {
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
| `operationId` | string | yes | Long-running operation identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "done": true,
      "error": {},
      "metadata": {},
      "name": "Ava Chen",
      "response": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `done` | boolean | Whether the long-running operation is complete. |
| `error` | object | Operation error details, when present. |
| `metadata` | object | Service-specific operation metadata. |
| `name` | string | Server-assigned operation name. |
| `response` | object | Service-specific operation response. |

## Native endpoint

Through the native Firebase API, this operation is `GET /v1beta1/operations/[:operationId]` (base URL `https://firebase.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-operation.md) for the provider-specific parameters and requirements.

