# Harvestr.io: Create User



```
POST https://connect.mindcloud.co/v1/universal/harvestr/latest/actions/create-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Harvestr.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/harvestr/latest/actions/create-user" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/harvestr/latest/actions/create-user', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | The name of the user |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email` | string | no | The email address of the user |
| `externalUid` | string | no | External unique identifier for the user from an external system |
| `phone` | string | no | Phone number of the user |
| `segments[]` | array<string> | no | Array of segment names the user belongs to |
| `segments[]` | array<string> | no | Array of segment names the user belongs to |
| `segments[]` | array<string> | no | Array of segment names the user belongs to |
| `segments[]` | array<string> | no | Array of segment names the user belongs to |
| `segments[]` | array<string> | no | Array of segment names the user belongs to |
| `companyId` | string | no | ID of the company the user belongs to |

## Response

```json
{
  "success": true,
  "data": [
    {
      "clientId": "string",
      "companyId": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "externalUid": "string",
      "id": "string",
      "importId": "string",
      "name": "Ava Chen",
      "phone": "string",
      "segments": {
        "clientId": "string",
        "createdAt": "2026-05-07T12:00:00.000Z",
        "id": "string",
        "name": "Ava Chen",
        "updatedAt": "2026-05-07T12:00:00.000Z"
      },
      "type": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `clientId` | string | Client identifier |
| `companyId` | string | Identifier of the company the user belongs to |
| `createdAt` | date | Creation date of the user |
| `email` | string | Email address of the user (can be empty) |
| `externalUid` | string | Only defined when external uid has been setup in Harvestr and when the entity has an external uid in source |
| `id` | string | Unique identifier of the user |
| `importId` | string | Only defined when the user was created from XLSX import, equal to its defined ID |
| `name` | string | Name of the user |
| `phone` | string | Phone number of the user |
| `segments` | array<object> | Segments associated with this user |
| `segments.clientId` | string | Client identifier |
| `segments.createdAt` | date | Creation date of the segment |
| `segments.id` | string | Unique identifier of the segment |
| `segments.name` | string | Name of the segment |
| `segments.updatedAt` | date | Last update date of the segment |
| `type` | string | Type of the user |
| `updatedAt` | date | Last update date of the user |

## Native endpoint

Through the native Harvestr.io API, this operation is `POST /user` (base URL `https://rest.harvestr.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-user.md) for the provider-specific parameters and requirements.

