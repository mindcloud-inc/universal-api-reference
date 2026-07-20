# iubenda: Get Consent

Retrieves a consent from iubenda.

```
GET https://connect.mindcloud.co/v1/universal/iubenda/latest/actions/get-consent
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a iubenda `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/iubenda/latest/actions/get-consent?connectionId=$CONNECTION_ID&consentId=73430ae8-6382-42e3-8c57-943f59867467" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "consentId": "73430ae8-6382-42e3-8c57-943f59867467"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/iubenda/latest/actions/get-consent?${params}`, {
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
| `consentId` | string | yes | Unique identifier of the consent event Example: `73430ae8-6382-42e3-8c57-943f59867467`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "ip_address": "string",
      "legal_notices": [
        {}
      ],
      "owner": "string",
      "preferences": {},
      "proof_documents": [
        "string"
      ],
      "proofs": [
        {}
      ],
      "source": "string",
      "subject": {},
      "timestamp": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `ip_address` | string |  |
| `legal_notices` | array<object> |  |
| `owner` | string |  |
| `preferences` | object |  |
| `proof_documents` | array |  |
| `proofs` | array<object> |  |
| `source` | string |  |
| `subject` | object |  |
| `timestamp` | string |  |

## Native endpoint

Through the native iubenda API, this operation is `GET /consent/:id` (base URL `https://consent.iubenda.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-consent.md) for the provider-specific parameters and requirements.

