# Ziflow: Get Contact

Retrieves a contact from Ziflow by ID or email.

```
GET https://connect.mindcloud.co/v1/universal/ziflow/latest/actions/get-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ziflow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ziflow/latest/actions/get-contact?connectionId=$CONNECTION_ID&identifier=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "identifier": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ziflow/latest/actions/get-contact?${params}`, {
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
| `identifier` | string | yes | Contact identifier (ID or email). |

## Response

```json
{
  "success": true,
  "data": [
    {
      "blocked": true,
      "company": "string",
      "email": "ava@example.com",
      "first_name": "Ava",
      "id": "string",
      "language": "string",
      "last_name": "Chen",
      "phone": "string",
      "proofing_defaults": {
        "comment": true,
        "decision": true,
        "manage": true,
        "notification": "string",
        "share": true,
        "view": true
      },
      "roles": [
        "string"
      ],
      "tenant": {
        "company_name": "Ava Chen",
        "subdomain": "string",
        "tenant_id": "string"
      },
      "timezone": "string",
      "type": "string",
      "verified": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `blocked` | boolean |  |
| `company` | string |  |
| `email` | string |  |
| `first_name` | string |  |
| `id` | string |  |
| `language` | string |  |
| `last_name` | string |  |
| `phone` | string |  |
| `proofing_defaults.comment` | boolean |  |
| `proofing_defaults.decision` | boolean |  |
| `proofing_defaults.manage` | boolean |  |
| `proofing_defaults.notification` | string |  |
| `proofing_defaults.share` | boolean |  |
| `proofing_defaults.view` | boolean |  |
| `roles[]` | string |  |
| `tenant.company_name` | string |  |
| `tenant.subdomain` | string |  |
| `tenant.tenant_id` | string |  |
| `timezone` | string |  |
| `type` | string |  |
| `verified` | boolean |  |

## Native endpoint

Through the native Ziflow API, this operation is `GET /contacts/:identifier` (base URL `https://api.ziflow.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-contact.md) for the provider-specific parameters and requirements.

