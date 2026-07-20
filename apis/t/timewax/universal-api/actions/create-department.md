# Timewax: Create Department

Creates a new department in Timewax.

```
POST https://connect.mindcloud.co/v1/universal/timewax/latest/actions/create-department
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Timewax `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/timewax/latest/actions/create-department" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "request.code": "string",
  "request.name": "Ava Chen",
  "request.manager": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/timewax/latest/actions/create-department', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "request.code": "string",
    "request.name": "Ava Chen",
    "request.manager": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `request.code` | string | yes | Required. Code of the department. |
| `request.name` | string | yes | Required. Name of the department. |
| `request.manager` | string | yes | Required. Code or name of the resource that is the department manager. |

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

Through the native Timewax API, this operation is `POST department/add/` (base URL `https://api.timewax.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-department.md) for the provider-specific parameters and requirements.

