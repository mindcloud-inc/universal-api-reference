# retailCRM: List Sites

Retrieves sites from retailCRM.

```
GET https://connect.mindcloud.co/v1/universal/retailCRM/latest/actions/list-sites
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a retailCRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/retailCRM/latest/actions/list-sites?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/retailCRM/latest/actions/list-sites?${params}`, {
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
      "catalogId": "string",
      "code": "string",
      "countryIso": "string",
      "currency": "string",
      "defaultForCrm": true,
      "id": 1,
      "isCatalogMainSite": true,
      "isDemo": true,
      "loadFromYml": true,
      "name": "Ava Chen",
      "ordering": 1,
      "url": "https://example.com",
      "usedInSimlaweb": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `catalogId` | string |  |
| `code` | string |  |
| `countryIso` | string |  |
| `currency` | string |  |
| `defaultForCrm` | boolean |  |
| `id` | number |  |
| `isCatalogMainSite` | boolean |  |
| `isDemo` | boolean |  |
| `loadFromYml` | boolean |  |
| `name` | string |  |
| `ordering` | number |  |
| `url` | string |  |
| `usedInSimlaweb` | boolean |  |

## Native endpoint

Through the native retailCRM API, this operation is `GET /reference/sites` (base URL `{{credentials.accountUrl}}/api/v5`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-sites.md) for the provider-specific parameters and requirements.

