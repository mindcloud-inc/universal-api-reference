# Autentique: Get Current Organization

Retrieves the current organization from Autentique.

```
GET https://connect.mindcloud.co/v1/universal/autentique/latest/actions/get-current-organization
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Autentique `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/autentique/latest/actions/get-current-organization?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/autentique/latest/actions/get-current-organization?${params}`, {
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
      "id": 1,
      "name": "Ava Chen",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |
| `name` | string |  |
| `uuid` | string |  |

## Native endpoint

Through the native Autentique API, this operation is `POST` (base URL `https://api.autentique.com.br/v2/graphql`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-current-organization.md) for the provider-specific parameters and requirements.

