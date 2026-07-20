# Middesk: Retrieve a registration request

Retrieves a registration request from Middesk.

```
GET https://connect.mindcloud.co/v1/universal/middesk/latest/actions/get-registration-request
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Middesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/middesk/latest/actions/get-registration-request?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/middesk/latest/actions/get-registration-request?${params}`, {
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
| `id` | string | yes | ID of the registration request to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "agencies": [
        {}
      ],
      "companyId": "string",
      "createdAt": "string",
      "externalId": "string",
      "id": "string",
      "inviteLink": "https://example.com",
      "items": [
        {}
      ],
      "object": "string",
      "state": "string",
      "status": "string",
      "submittedAt": "string",
      "taxRegistration": {},
      "taxRegistrationTypes": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `agencies` | array<object> |  |
| `companyId` | string |  |
| `createdAt` | string |  |
| `externalId` | string |  |
| `id` | string |  |
| `inviteLink` | string |  |
| `items` | array<object> |  |
| `object` | string |  |
| `state` | string |  |
| `status` | string |  |
| `submittedAt` | string |  |
| `taxRegistration` | object |  |
| `taxRegistrationTypes` | array<string> |  |

## Native endpoint

Through the native Middesk API, this operation is `GET /partner/registration_requests/:id` (base URL `https://api.middesk.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-registration-request.md) for the provider-specific parameters and requirements.

