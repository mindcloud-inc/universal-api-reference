# CardClan: Validate Authentication

Retrieves user details for a valid CardClan integration key.

```
GET https://connect.mindcloud.co/v1/universal/cardClan/latest/actions/validate-authentication
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CardClan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cardClan/latest/actions/validate-authentication?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cardClan/latest/actions/validate-authentication?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "success": true,
      "user_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string | Authentication result message. |
| `success` | boolean | Whether bearer token authentication succeeded. |
| `user_id` | string | Authenticated CardClan user ID. |

## Native endpoint

Through the native CardClan API, this operation is `GET /integration/auth/validate` (base URL `https://app.cardclan.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/validate-authentication.md) for the provider-specific parameters and requirements.

