# ManyReach: Get Clientspace

Retrieves a clientspace from ManyReach.

```
GET https://connect.mindcloud.co/v1/universal/manyReach/latest/actions/get-clientspace
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ManyReach `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/manyReach/latest/actions/get-clientspace?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/manyReach/latest/actions/get-clientspace?${params}`, {
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
| `id` | string | yes | The ID of the clientspace to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "apiKey": "string",
      "autoAllocate": true,
      "clientspaceId": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "creditAmount": 1,
      "separateCredits": true,
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `apiKey` | string |  |
| `autoAllocate` | boolean |  |
| `clientspaceId` | number |  |
| `createdAt` | date |  |
| `creditAmount` | number |  |
| `separateCredits` | boolean |  |
| `title` | string |  |

## Native endpoint

Through the native ManyReach API, this operation is `GET https://api.manyreach.com/api/v2/clientspaces/:id` (base URL `https://api.manyreach.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-clientspace.md) for the provider-specific parameters and requirements.

