# Picnie: Create Project

Creates a new project in Picnie.

```
POST https://connect.mindcloud.co/v1/universal/picnie/latest/actions/create-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Picnie `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/picnie/latest/actions/create-project" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Project API Test 2026-03-30"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/picnie/latest/actions/create-project', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Project API Test 2026-03-30"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Name of the project to create. Example: `Project API Test 2026-03-30`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {
          "datetimeCreated": "string",
          "id": "string",
          "isActive": "string",
          "name": "Ava Chen",
          "type": "string",
          "userId": "string"
        }
      ],
      "error": true,
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data[].datetimeCreated` | string |  |
| `data[].id` | string |  |
| `data[].isActive` | string |  |
| `data[].name` | string |  |
| `data[].type` | string |  |
| `data[].userId` | string |  |
| `error` | boolean |  |
| `message` | string |  |

## Native endpoint

Through the native Picnie API, this operation is `POST /create-project` (base URL `https://picnie.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-project.md) for the provider-specific parameters and requirements.

