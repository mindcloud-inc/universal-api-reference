# Themeforest: Get User Profile

Retrieves profile details for an Envato user.

```
GET https://connect.mindcloud.co/v1/universal/themeForest/latest/actions/get-user-profile
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Themeforest `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/themeForest/latest/actions/get-user-profile?connectionId=$CONNECTION_ID&username=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "username": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/themeForest/latest/actions/get-user-profile?${params}`, {
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
| `username` | string | yes | Envato username. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "homepage": "string",
      "image": "string",
      "sales": 1,
      "username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `homepage` | string | User homepage URL. |
| `image` | string | Profile image URL. |
| `sales` | number | Sales count when returned. |
| `username` | string | Envato username. |

## Native endpoint

Through the native Themeforest API, this operation is `GET /v1/market/user::username.json` (base URL `https://api.envato.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user-profile.md) for the provider-specific parameters and requirements.

