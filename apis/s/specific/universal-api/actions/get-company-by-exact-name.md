# Specific: Get Company By Exact Name

Retrieves a company from Specific by exact name.

```
GET https://connect.mindcloud.co/v1/universal/specific/latest/actions/get-company-by-exact-name
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Specific `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/specific/latest/actions/get-company-by-exact-name?connectionId=$CONNECTION_ID&variables.name=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "variables.name": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/specific/latest/actions/get-company-by-exact-name?${params}`, {
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
| `variables.name` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "name": "Ava Chen",
      "usersCount": 1,
      "visitorId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `name` | string |  |
| `usersCount` | number |  |
| `visitorId` | string |  |

## Native endpoint

Through the native Specific API, this operation is `POST` (base URL `https://public-api.specific.app/graphql`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-company-by-exact-name.md) for the provider-specific parameters and requirements.

