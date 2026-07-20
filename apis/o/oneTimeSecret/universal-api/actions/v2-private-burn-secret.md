# One-Time Secret: Private Burn Secret

Deletes a private secret from One-Time Secret by receipt identifier.

```
DELETE https://connect.mindcloud.co/v1/universal/oneTimeSecret/latest/actions/v2-private-burn-secret
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a One-Time Secret `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/oneTimeSecret/latest/actions/v2-private-burn-secret?connectionId=$CONNECTION_ID&identifier=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "identifier": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oneTimeSecret/latest/actions/v2-private-burn-secret?${params}`, {
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
| `identifier` | string | yes | Private receipt identifier for the secret to burn. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `continue` | string | no | Provider confirmation token when required to proceed with private burn. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "details": {},
      "record": {},
      "shrimp": "string",
      "user_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `details` | object | Private burn result details. |
| `record` | object | Burned private receipt record. |
| `shrimp` | string | Provider response marker when returned. |
| `user_id` | string | Authenticated user identifier when returned. |

## Native endpoint

Through the native One-Time Secret API, this operation is `POST /api/v2/private/:identifier/burn` (base URL `https://us.onetimesecret.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/v2-private-burn-secret.md) for the provider-specific parameters and requirements.

