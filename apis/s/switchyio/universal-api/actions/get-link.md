# Switchy.io: Get Link

Retrieves a link from Switchy.io by domain and ID.

```
GET https://connect.mindcloud.co/v1/universal/switchyio/latest/actions/get-link
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Switchy.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/switchyio/latest/actions/get-link?connectionId=$CONNECTION_ID&domain=string&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "domain": "string",
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/switchyio/latest/actions/get-link?${params}`, {
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
| `domain` | string | yes |  |
| `id` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "clicks": 1,
      "createdDate": "2026-05-07T12:00:00.000Z",
      "domain": "string",
      "id": "string",
      "name": "Ava Chen",
      "tags": [
        "string"
      ],
      "title": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `clicks` | number |  |
| `createdDate` | date |  |
| `domain` | string |  |
| `id` | string |  |
| `name` | string |  |
| `tags` | array<string> |  |
| `title` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Switchy.io API, this operation is `POST /v1/graphql` (base URL `https://graphql.switchy.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-link.md) for the provider-specific parameters and requirements.

