# Specific: Get User By Email

Retrieves a user from Specific by email.

```
GET https://connect.mindcloud.co/v1/universal/specific/latest/actions/get-user-by-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Specific `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/specific/latest/actions/get-user-by-email?connectionId=$CONNECTION_ID&variables.email=ava%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "variables.email": "ava@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/specific/latest/actions/get-user-by-email?${params}`, {
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
| `variables.email` | string | yes |  |

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

Through the native Specific API, this operation is `POST` (base URL `https://public-api.specific.app/graphql`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user-by-email.md) for the provider-specific parameters and requirements.

