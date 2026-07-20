# Userback: Update Project

Updates a Userback project.

```
PUT https://connect.mindcloud.co/v1/universal/userback/latest/actions/update-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Userback `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/userback/latest/actions/update-project" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "137605"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/userback/latest/actions/update-project', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "137605"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | The project ID to update. Example: `137605`. |
| `name` | string | no | The updated project name. Example: `My first project`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `url` | string | no | The updated project URL. Example: `https://example.com`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created": "string",
      "createdBy": 1,
      "id": 1,
      "isArchived": true,
      "name": "Ava Chen",
      "projectType": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | string |  |
| `createdBy` | number |  |
| `id` | number |  |
| `isArchived` | boolean |  |
| `name` | string |  |
| `projectType` | string |  |

## Native endpoint

Through the native Userback API, this operation is `PATCH /project/:id` (base URL `https://rest.userback.io/1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-project.md) for the provider-specific parameters and requirements.

