# Billforward: Find Account By Email

Finds an account in Billforward by email address.

```
GET https://connect.mindcloud.co/v1/universal/billforward/latest/actions/find-account-by-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Billforward `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/billforward/latest/actions/find-account-by-email?connectionId=$CONNECTION_ID&email=ava%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "email": "ava@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/billforward/latest/actions/find-account-by-email?${params}`, {
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
| `email` | string | yes | The Billforward account email to search for. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Billforward API returns.

## Native endpoint

Through the native Billforward API, this operation is `GET /accounts/email/:email` (base URL `https://app-sandbox.billforward.net/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/find-account-by-email.md) for the provider-specific parameters and requirements.

