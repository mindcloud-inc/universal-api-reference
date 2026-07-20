# Pabbly Hook: Create Transformation



```
POST https://connect.mindcloud.co/v1/universal/pabblyHook/latest/actions/create-transformation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pabbly Hook `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pabblyHook/latest/actions/create-transformation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Normalize checkout payload",
  "code": "(request, context) => { return request; }"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pabblyHook/latest/actions/create-transformation', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Normalize checkout payload",
    "code": "(request, context) => { return request; }"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Transformation name. Example: `Normalize checkout payload`. |
| `code` | string | yes | Transformation JavaScript code. Example: `(request, context) => { return request; }`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "Id": "string",
      "name": "Ava Chen",
      "trsId": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "userId": "string",
      "v": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | string | Transformation JavaScript code. |
| `createdAt` | date | Creation timestamp. |
| `Id` | string | Pabbly Hook internal transformation identifier. |
| `name` | string | Transformation name. |
| `trsId` | string | Public Pabbly Hook transformation identifier. |
| `updatedAt` | date | Last update timestamp. |
| `userId` | string | Pabbly account user identifier. |
| `v` | number | Provider version counter. |

## Native endpoint

Through the native Pabbly Hook API, this operation is `POST /api/v1/transformations` (base URL `https://hook.pabbly.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-transformation.md) for the provider-specific parameters and requirements.

