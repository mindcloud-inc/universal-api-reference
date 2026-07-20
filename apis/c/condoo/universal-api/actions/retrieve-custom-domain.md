# condoo: Retrieve Custom Domain

Retrieves a custom domain from condoo.

```
GET https://connect.mindcloud.co/v1/universal/condoo/latest/actions/retrieve-custom-domain
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a condoo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/condoo/latest/actions/retrieve-custom-domain?connectionId=$CONNECTION_ID&domainId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "domainId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/condoo/latest/actions/retrieve-custom-domain?${params}`, {
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
| `domainId` | number | yes | Required custom domain ID. |

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

Through the native condoo API, this operation is `GET /domains/{domain_id}` (base URL `https://trk.condoo.systems/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-custom-domain.md) for the provider-specific parameters and requirements.

