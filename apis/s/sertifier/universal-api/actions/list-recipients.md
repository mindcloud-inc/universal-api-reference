# Sertifier: List Recipients

Finds recipients in Sertifier by search filters.

```
GET https://connect.mindcloud.co/v1/universal/sertifier/latest/actions/list-recipients
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sertifier `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sertifier/latest/actions/list-recipients?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sertifier/latest/actions/list-recipients?${params}`, {
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
| `startIndex` | number | no | Default: `0`. |
| `length` | number | no | Default: `10`. |
| `searchTerm` | string | no | Example: `recipient email or name`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "email": "ava@example.com",
      "externalID": {},
      "id": "string",
      "name": "Ava Chen",
      "profileUrl": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `email` | string |  |
| `externalID` | object |  |
| `id` | string |  |
| `name` | string |  |
| `profileUrl` | object |  |

## Native endpoint

Through the native Sertifier API, this operation is `POST /recipient/search` (base URL `https://b2b.sertifier.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-recipients.md) for the provider-specific parameters and requirements.

