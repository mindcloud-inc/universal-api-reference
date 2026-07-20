# Harness: List Service Accounts

Retrieves service accounts from Harness.

```
GET https://connect.mindcloud.co/v1/universal/harness/latest/actions/list-service-accounts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Harness `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/harness/latest/actions/list-service-accounts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/harness/latest/actions/list-service-accounts?${params}`, {
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
| `identifiers` | list<string> | no | Service account identifiers to include. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "email": "ava@example.com",
      "identifier": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `email` | string | Service account email. |
| `identifier` | string | Service account identifier. |
| `name` | string | Service account name. |

## Native endpoint

Through the native Harness API, this operation is `GET /ng/api/serviceaccount` (base URL `https://app.harness.io/gateway`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-service-accounts.md) for the provider-specific parameters and requirements.

