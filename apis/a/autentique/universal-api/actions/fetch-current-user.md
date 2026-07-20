# Autentique: Fetch Current User

Retrieves the current user from Autentique.

```
GET https://connect.mindcloud.co/v1/universal/autentique/latest/actions/fetch-current-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Autentique `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/autentique/latest/actions/fetch-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/autentique/latest/actions/fetch-current-user?${params}`, {
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
      "email": "ava@example.com",
      "id": "string",
      "name": "Ava Chen",
      "organization": {
        "id": 1,
        "name": "Ava Chen",
        "uuid": "string"
      },
      "subscription": {
        "credits": 1,
        "documents": 1,
        "hasPremiumFeatures": true
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `email` | string |  |
| `id` | string |  |
| `name` | string |  |
| `organization.id` | number |  |
| `organization.name` | string |  |
| `organization.uuid` | string |  |
| `subscription.credits` | number |  |
| `subscription.documents` | number |  |
| `subscription.hasPremiumFeatures` | boolean |  |

## Native endpoint

Through the native Autentique API, this operation is `POST` (base URL `https://api.autentique.com.br/v2/graphql`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/fetch-current-user.md) for the provider-specific parameters and requirements.

