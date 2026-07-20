# IdentityCheck: Get Public Onboarding Form



```
GET https://connect.mindcloud.co/v1/universal/identityCheck/latest/actions/get-public-onboarding-form
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a IdentityCheck `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/identityCheck/latest/actions/get-public-onboarding-form?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/identityCheck/latest/actions/get-public-onboarding-form?${params}`, {
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
| `id` | string | yes | Public onboarding identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "abort": {
        "name": "Ava Chen",
        "redirect_url": "https://example.com",
        "type": "string"
      },
      "tfns": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `abort.name` | string |  |
| `abort.redirect_url` | string |  |
| `abort.type` | string |  |
| `tfns` | string |  |

## Native endpoint

Through the native IdentityCheck API, this operation is `GET /public/onboarding/{id}` (base URL `https://identity.stackgo.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-public-onboarding-form.md) for the provider-specific parameters and requirements.

