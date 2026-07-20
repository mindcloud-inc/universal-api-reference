# Linkbreakers: Get a Visitor

Retrieves detailed visitor information from Linkbreakers.

```
GET https://connect.mindcloud.co/v1/universal/linkbreakers/latest/actions/get-visitor
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Linkbreakers `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/linkbreakers/latest/actions/get-visitor?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/linkbreakers/latest/actions/get-visitor?${params}`, {
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
| `id` | string | yes | The ID of the visitor to retrieve. |
| `include[]` | array<string> | no | Relationships to include in the visitor response. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {},
      "createdAt": "string",
      "devices": [
        {}
      ],
      "email": "ava@example.com",
      "events": [
        {}
      ],
      "firstName": "Ava",
      "id": "string",
      "lastName": "Chen",
      "links": [
        {}
      ],
      "phone": "string",
      "updatedAt": "string",
      "workspaceId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes` | object |  |
| `createdAt` | string |  |
| `devices` | array<object> |  |
| `email` | string |  |
| `events` | array<object> |  |
| `firstName` | string |  |
| `id` | string |  |
| `lastName` | string |  |
| `links` | array<object> |  |
| `phone` | string |  |
| `updatedAt` | string |  |
| `workspaceId` | string |  |

## Native endpoint

Through the native Linkbreakers API, this operation is `GET /v1/visitors/:id` (base URL `https://api.linkbreakers.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-visitor.md) for the provider-specific parameters and requirements.

