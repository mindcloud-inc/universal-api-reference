# Goodbarber eCommerce: Validate Front JWT



```
GET https://connect.mindcloud.co/v1/universal/goodbarberECommerce/latest/actions/validate-front-jwt
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Goodbarber eCommerce `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/goodbarberECommerce/latest/actions/validate-front-jwt?connectionId=$CONNECTION_ID&userId=11310&jwt=replace-me-front-jwt" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "userId": "11310",
  "jwt": "replace-me-front-jwt"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/goodbarberECommerce/latest/actions/validate-front-jwt?${params}`, {
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
| `userId` | string | yes | Unique ID of the user against which the token should be validated. Default: `11310`. Example: `11310`. |
| `jwt` | string | yes | Token to validate. Default: `replace-me-front-jwt`. Example: `replace-me-front-jwt`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "is_anonymous": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `is_anonymous` | boolean | <div class="field_description">Indicates whether the user associated with the token is anonymous or not.</div> |

## Native endpoint

Through the native Goodbarber eCommerce API, this operation is `POST /publicapi/v2/general/customer/:webzine_id/auth/validate/` (base URL `https://commerce.goodbarber.dev`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/validate-front-jwt.md) for the provider-specific parameters and requirements.

