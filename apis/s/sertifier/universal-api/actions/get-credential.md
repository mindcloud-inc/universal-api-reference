# Sertifier: Get Credential

Retrieves a credential from a Sertifier workspace.

```
GET https://connect.mindcloud.co/v1/universal/sertifier/latest/actions/get-credential
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sertifier `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sertifier/latest/actions/get-credential?connectionId=$CONNECTION_ID&credential_id=Credential%20ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "credential_id": "Credential ID"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sertifier/latest/actions/get-credential?${params}`, {
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
| `credential_id` | string | yes | Example: `Credential ID`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "badgeImageLink": {},
      "certificateImageLink": {},
      "certificateNO": "string",
      "createDate": "string",
      "email": {},
      "emailTracking": 1,
      "expireDate": {},
      "id": "string",
      "isPublic": true,
      "issueDate": "string",
      "name": "Ava Chen",
      "recipientId": "string",
      "status": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `badgeImageLink` | object |  |
| `certificateImageLink` | object |  |
| `certificateNO` | string |  |
| `createDate` | string |  |
| `email` | object |  |
| `emailTracking` | number |  |
| `expireDate` | object |  |
| `id` | string |  |
| `isPublic` | boolean |  |
| `issueDate` | string |  |
| `name` | string |  |
| `recipientId` | string |  |
| `status` | number |  |

## Native endpoint

Through the native Sertifier API, this operation is `GET /credential/:credential_id` (base URL `https://b2b.sertifier.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-credential.md) for the provider-specific parameters and requirements.

