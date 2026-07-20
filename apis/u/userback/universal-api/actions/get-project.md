# Userback: Get Project

Retrieves a Userback project by ID.

```
GET https://connect.mindcloud.co/v1/universal/userback/latest/actions/get-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Userback `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/userback/latest/actions/get-project?connectionId=$CONNECTION_ID&id=137605" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "137605"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/userback/latest/actions/get-project?${params}`, {
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
| `id` | number | yes | The project ID to retrieve. Example: `137605`. |

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
      "members": [
        {
          "email": "ava@example.com",
          "id": 1,
          "isDisabled": true,
          "name": "Ava Chen",
          "role": "string",
          "userId": 1
        }
      ],
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
| `members[].email` | string |  |
| `members[].id` | number |  |
| `members[].isDisabled` | boolean |  |
| `members[].name` | string |  |
| `members[].role` | string |  |
| `members[].userId` | number |  |
| `name` | string |  |
| `projectType` | string |  |

## Native endpoint

Through the native Userback API, this operation is `GET /project/:id` (base URL `https://rest.userback.io/1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-project.md) for the provider-specific parameters and requirements.

