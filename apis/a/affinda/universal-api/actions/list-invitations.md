# Affinda: Get list of all invitations

Retrieves all accessible invitations from Affinda.

```
GET https://connect.mindcloud.co/v1/universal/affinda/latest/actions/list-invitations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Affinda `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/affinda/latest/actions/list-invitations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/affinda/latest/actions/list-invitations?${params}`, {
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
| `limit` | string | no | The numbers of results to return. |
| `offset` | string | no | The number of documents to skip before starting to collect the result set. |
| `organization` | string | no | Filter by organization. |
| `role` | string | no | Filter by role. |
| `status` | string | no | Filter by status. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdDt": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "expiryDate": "2026-05-07T12:00:00.000Z",
      "identifier": "string",
      "invitedBy": {},
      "organization": {},
      "respondedBy": {},
      "role": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdDt` | date |  |
| `email` | string |  |
| `expiryDate` | date |  |
| `identifier` | string |  |
| `invitedBy` | object |  |
| `organization` | object |  |
| `respondedBy` | object |  |
| `role` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Affinda API, this operation is `GET /v3/invitations` (base URL `https://api.us1.affinda.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-invitations.md) for the provider-specific parameters and requirements.

