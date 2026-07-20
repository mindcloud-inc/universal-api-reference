# Specific: Search Users By ID Contains

Finds users in Specific by partial ID.

```
GET https://connect.mindcloud.co/v1/universal/specific/latest/actions/search-users-by-id-contains
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Specific `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/specific/latest/actions/search-users-by-id-contains?connectionId=$CONNECTION_ID&variables.id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "variables.id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/specific/latest/actions/search-users-by-id-contains?${params}`, {
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
| `variables.id` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "company": {
        "id": "string",
        "name": "Ava Chen"
      },
      "email": "ava@example.com",
      "id": "string",
      "name": "Ava Chen",
      "visitorId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `company.id` | string |  |
| `company.name` | string |  |
| `email` | string |  |
| `id` | string |  |
| `name` | string |  |
| `visitorId` | string |  |

## Native endpoint

Through the native Specific API, this operation is `POST` (base URL `https://public-api.specific.app/graphql`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-users-by-id-contains.md) for the provider-specific parameters and requirements.

