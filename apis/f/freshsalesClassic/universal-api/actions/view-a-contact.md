# Freshsales Classic: View a Contact

Retrieves a contact from Freshsales Classic.

```
GET https://connect.mindcloud.co/v1/universal/freshsalesClassic/latest/actions/view-a-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Freshsales Classic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/freshsalesClassic/latest/actions/view-a-contact?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/freshsalesClassic/latest/actions/view-a-contact?${params}`, {
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
| `id` | number | yes | The contact ID. |
| `include` | string | no | Optional related resources to embed in the contact response. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": "string",
      "city": "string",
      "country": "string",
      "createdAt": "string",
      "displayName": "Ava Chen",
      "email": "ava@example.com",
      "firstName": "Ava",
      "id": 1,
      "jobTitle": "string",
      "lastName": "Chen",
      "leadScore": 1,
      "mobileNumber": "string",
      "openDealsAmount": "string",
      "state": "string",
      "tags": [
        "string"
      ],
      "updatedAt": "string",
      "wonDealsAmount": "string",
      "workNumber": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | string |  |
| `city` | string |  |
| `country` | string |  |
| `createdAt` | string |  |
| `displayName` | string |  |
| `email` | string |  |
| `firstName` | string |  |
| `id` | number |  |
| `jobTitle` | string |  |
| `lastName` | string |  |
| `leadScore` | number |  |
| `mobileNumber` | string |  |
| `openDealsAmount` | string |  |
| `state` | string |  |
| `tags` | array<string> |  |
| `updatedAt` | string |  |
| `wonDealsAmount` | string |  |
| `workNumber` | string |  |

## Native endpoint

Through the native Freshsales Classic API, this operation is `GET /contacts/:id` (base URL `https://{{credentials.bundleAlias}}/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/view-a-contact.md) for the provider-specific parameters and requirements.

