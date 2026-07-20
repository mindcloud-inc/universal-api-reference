# Reward Sciences: Get User By External Identity



```
GET https://connect.mindcloud.co/v1/universal/rewardSciences/latest/actions/get-user-by-external-identity
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reward Sciences `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rewardSciences/latest/actions/get-user-by-external-identity?connectionId=$CONNECTION_ID&idp=string&identity=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "idp": "string",
  "identity": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rewardSciences/latest/actions/get-user-by-external-identity?${params}`, {
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
| `idp` | string | yes | Identity provider name. |
| `identity` | string | yes | Identity value within the provider. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "user_id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `user_id` | number | Resolved Reward Sciences user ID. |

## Native endpoint

Through the native Reward Sciences API, this operation is `GET /idps/:idp/:identity/user` (base URL `https://api.rewardsciences.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user-by-external-identity.md) for the provider-specific parameters and requirements.

