# One-Time Secret: Show Secret

Retrieves secret metadata from One-Time Secret by identifier.

```
GET https://connect.mindcloud.co/v1/universal/oneTimeSecret/latest/actions/v2-show-secret
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a One-Time Secret `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oneTimeSecret/latest/actions/v2-show-secret?connectionId=$CONNECTION_ID&identifier=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "identifier": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oneTimeSecret/latest/actions/v2-show-secret?${params}`, {
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
| `identifier` | string | yes | Secret identifier to retrieve. |

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
| `details` | object | Secret display and reveal metadata. |
| `record` | object | Secret record returned by One-Time Secret. |
| `shrimp` | string | Provider response marker when returned. |
| `user_id` | string | Authenticated user identifier when returned. |

## Native endpoint

Through the native One-Time Secret API, this operation is `GET /api/v2/secret/:identifier` (base URL `https://us.onetimesecret.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/v2-show-secret.md) for the provider-specific parameters and requirements.

