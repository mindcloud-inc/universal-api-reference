# Timewax: Create Resource

Creates a new resource in Timewax.

```
POST https://connect.mindcloud.co/v1/universal/timewax/latest/actions/create-resource
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Timewax `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/timewax/latest/actions/create-resource" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "request.code": "string",
  "request.lastName": "Chen",
  "request.firstNames": "Ava",
  "request.organisationalUnit": "string",
  "request.position": "string",
  "request.startDate": "2026-05-07T12:00:00.000Z"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/timewax/latest/actions/create-resource', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "request.code": "string",
    "request.lastName": "Chen",
    "request.firstNames": "Ava",
    "request.organisationalUnit": "string",
    "request.position": "string",
    "request.startDate": "2026-05-07T12:00:00.000Z"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `request.code` | string | yes | Code of the resource. |
| `request.lastName` | string | yes | Last name of the resource. |
| `request.firstNames` | string | yes | First name(s) of the resource. |
| `request.organisationalUnit` | string | yes | Code or name of the department. |
| `request.position` | string | yes | Code or name of the position. |
| `request.startDate` | date | yes | Start date for the resource. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "valid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `valid` | string | Operation validity indicator. |

## Native endpoint

Through the native Timewax API, this operation is `POST resource/add/` (base URL `https://api.timewax.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-resource.md) for the provider-specific parameters and requirements.

