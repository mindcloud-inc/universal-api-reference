# condoo: List Custom Domains

Retrieves custom domains from condoo.

```
GET https://connect.mindcloud.co/v1/universal/condoo/latest/actions/list-custom-domains
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a condoo `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/condoo/latest/actions/list-custom-domains?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/condoo/latest/actions/list-custom-domains?${params}`, {
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
| `isEnabled` | boolean | no | Optional enabled-state selector. |
| `search` | string | no | Optional search string. |
| `searchBy` | string | no | Optional search field. Allowed value: host. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "custom_index_url": "https://example.com",
      "custom_not_found_url": "https://example.com",
      "date": "2026-05-07T12:00:00.000Z",
      "datetime": "2026-05-07T12:00:00.000Z",
      "host": "string",
      "id": 1,
      "is_enabled": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `custom_index_url` | string |  |
| `custom_not_found_url` | string |  |
| `date` | date |  |
| `datetime` | date |  |
| `host` | string |  |
| `id` | number |  |
| `is_enabled` | boolean |  |

## Native endpoint

Through the native condoo API, this operation is `GET /domains/` (base URL `https://trk.condoo.systems/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-custom-domains.md) for the provider-specific parameters and requirements.

