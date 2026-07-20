# IdentityCheck: Submit Public Onboarding Form



```
POST https://connect.mindcloud.co/v1/universal/identityCheck/latest/actions/submit-public-onboarding-form
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a IdentityCheck `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/identityCheck/latest/actions/submit-public-onboarding-form" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/identityCheck/latest/actions/submit-public-onboarding-form', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Public onboarding identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "redirect": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `redirect` | string |  |

## Native endpoint

Through the native IdentityCheck API, this operation is `POST /public/onboarding/{id}` (base URL `https://identity.stackgo.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/submit-public-onboarding-form.md) for the provider-specific parameters and requirements.

