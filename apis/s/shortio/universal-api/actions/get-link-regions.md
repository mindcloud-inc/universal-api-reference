# Short.io: Get Link Regions

Retrieves link regions from Short.io.

```
GET https://connect.mindcloud.co/v1/universal/shortio/latest/actions/get-link-regions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Short.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shortio/latest/actions/get-link-regions?connectionId=$CONNECTION_ID&linkId=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "linkId": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shortio/latest/actions/get-link-regions?${params}`, {
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
| `linkId` | string | yes |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `domainId` | string | no | Domain ID |

## Response

```json
{
  "success": true,
  "data": [
    {
      "country": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "linkIdString": "https://example.com",
      "name": "Ava Chen",
      "originalURL": "https://example.com",
      "region": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `country` | string |  |
| `createdAt` | date |  |
| `id` | number |  |
| `linkIdString` | string |  |
| `name` | string |  |
| `originalURL` | string |  |
| `region` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Short.io API, this operation is `GET /link_region/:linkId` (base URL `https://api.short.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-link-regions.md) for the provider-specific parameters and requirements.

