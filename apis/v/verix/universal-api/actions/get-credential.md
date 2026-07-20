# Verix: Get Credential

Retrieves a credential from your Verix account.

```
GET https://connect.mindcloud.co/v1/universal/verix/latest/actions/get-credential
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Verix `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/verix/latest/actions/get-credential?connectionId=$CONNECTION_ID&credential_id=3145dfc827ed4c95aa6c5f2b80ac4008" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "credential_id": "3145dfc827ed4c95aa6c5f2b80ac4008"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/verix/latest/actions/get-credential?${params}`, {
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
| `credential_id` | string | yes | Credential ID to retrieve. Example: `3145dfc827ed4c95aa6c5f2b80ac4008`. |
| `format` | string | no | Set to json_input for nested JSON output. Default is csv_input. One of: `0`, `1`. Example: `json_input`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "credential": {
        "description": "string",
        "name": "Ava Chen",
        "validFrom": "string",
        "validUntil": "string"
      },
      "custom": {},
      "recipient": {
        "email": "ava@example.com",
        "externalId": "string",
        "name": "Ava Chen"
      },
      "subject": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `credential` | object | Credential details. |
| `credential.description` | string | Credential description. |
| `credential.name` | string | Credential name. |
| `credential.validFrom` | string | ISO timestamp when the credential becomes valid. |
| `credential.validUntil` | string | ISO timestamp when the credential expires. |
| `custom` | object | Custom fields stored on the credential. |
| `recipient` | object | Recipient details. |
| `recipient.email` | string | Recipient email address. |
| `recipient.externalId` | string | Recipient external identifier. |
| `recipient.name` | string | Recipient full name. |
| `subject` | object | Credential subject payload. |

## Native endpoint

Through the native Verix API, this operation is `GET /v1/credentials/:credential_id/` (base URL `https://api.verix.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-credential.md) for the provider-specific parameters and requirements.

