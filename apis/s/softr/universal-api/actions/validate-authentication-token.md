# Softr: Validate Authentication Token



```
GET https://connect.mindcloud.co/v1/universal/softr/latest/actions/validate-authentication-token
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Softr `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/softr/latest/actions/validate-authentication-token?connectionId=$CONNECTION_ID&jwt=eyJhbGciOi..." \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "jwt": "eyJhbGciOi..."
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/softr/latest/actions/validate-authentication-token?${params}`, {
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
| `jwt` | string | yes | JWT token for the Softr user session to validate. Example: `eyJhbGciOi...`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "isValid": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `isValid` | boolean |  |

## Native endpoint

Through the native Softr API, this operation is `POST https://priscilla41205.softr.app/v1/api/users/validate-token` (base URL `https://tables-api.softr.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/validate-authentication-token.md) for the provider-specific parameters and requirements.

