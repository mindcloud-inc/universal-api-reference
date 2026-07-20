# Postmaster+: Retrieve Single Email

Retrieves single email intelligence from Postmaster+.

```
GET https://connect.mindcloud.co/v1/universal/postmaster/latest/actions/retrieve-single-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Postmaster+ `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/postmaster/latest/actions/retrieve-single-email?connectionId=$CONNECTION_ID&email=ava%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "email": "ava@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/postmaster/latest/actions/retrieve-single-email?${params}`, {
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
| `email` | string | yes | The email address to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "email": "ava@example.com",
      "id": 1,
      "message": "string",
      "status": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string | Creation timestamp. |
| `email` | string | Email address. |
| `id` | number | Single email record ID. |
| `message` | string | Provider message for non-success cases. |
| `status` | string | Deliverability status. |
| `updatedAt` | string | Update timestamp. |

## Native endpoint

Through the native Postmaster+ API, this operation is `GET /api/v1/intelligence/single-emails/:email` (base URL `https://postmasterplus.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-single-email.md) for the provider-specific parameters and requirements.

