# IdentityCheck: Get Pre-Verification Setting



```
GET https://connect.mindcloud.co/v1/universal/identityCheck/latest/actions/get-pre-verification-setting
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a IdentityCheck `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/identityCheck/latest/actions/get-pre-verification-setting?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/identityCheck/latest/actions/get-pre-verification-setting?${params}`, {
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
| `id` | string | yes | IdentityCheck pre-verification setting identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "action": "string",
        "email": "ava@example.com",
        "namePattern": "Ava Chen",
        "notificationEmail": "ava@example.com",
        "redirectToVerification": true,
        "taxAgent": "string",
        "verifyIndividualIdentity": true
      },
      "enabled": true,
      "id": "string",
      "misc": {
        "form_id": "string"
      },
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.action` | string |  |
| `data.email` | string |  |
| `data.namePattern` | string |  |
| `data.notificationEmail` | string |  |
| `data.redirectToVerification` | boolean |  |
| `data.taxAgent` | string |  |
| `data.verifyIndividualIdentity` | boolean |  |
| `enabled` | boolean |  |
| `id` | string |  |
| `misc.form_id` | string |  |
| `name` | string |  |

## Native endpoint

Through the native IdentityCheck API, this operation is `GET /pre-verification-settings/{id}` (base URL `https://identity.stackgo.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-pre-verification-setting.md) for the provider-specific parameters and requirements.

