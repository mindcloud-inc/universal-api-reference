# folk: Create Person

Creates a new person in folk.

```
POST https://connect.mindcloud.co/v1/universal/folk/latest/actions/create-person
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a folk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/folk/latest/actions/create-person" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "fullName": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/folk/latest/actions/create-person', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "fullName": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fullName` | string | yes | The full name of the person. |
| `description` | string | no | A short description for the person. |
| `jobTitle` | string | no | The person's job title. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "addresses": [
        "string"
      ],
      "birthday": "2026-05-07T12:00:00.000Z",
      "companies": [
        {}
      ],
      "createdAt": "2026-05-07T12:00:00.000Z",
      "createdBy": {},
      "customFieldValues": {},
      "description": "string",
      "emails": [
        "ava@example.com"
      ],
      "firstName": "Ava",
      "fullName": "Ava Chen",
      "groups": [
        {}
      ],
      "id": "string",
      "interactionMetadata": {},
      "jobTitle": "string",
      "lastName": "Chen",
      "phones": [
        "string"
      ],
      "strongestConnection": {},
      "urls": [
        "https://example.com"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `addresses` | array<string> |  |
| `birthday` | date |  |
| `companies` | array<object> |  |
| `createdAt` | date |  |
| `createdBy` | object |  |
| `customFieldValues` | object |  |
| `description` | string |  |
| `emails` | array<string> |  |
| `firstName` | string |  |
| `fullName` | string |  |
| `groups` | array<object> |  |
| `id` | string |  |
| `interactionMetadata` | object |  |
| `jobTitle` | string |  |
| `lastName` | string |  |
| `phones` | array<string> |  |
| `strongestConnection` | object |  |
| `urls` | array<string> |  |

## Native endpoint

Through the native folk API, this operation is `POST /v1/people` (base URL `https://api.folk.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-person.md) for the provider-specific parameters and requirements.

