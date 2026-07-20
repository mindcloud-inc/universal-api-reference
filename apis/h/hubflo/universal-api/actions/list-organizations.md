# Hubflo: List Organizations

Retrieves all available organizations from Hubflo.

```
GET https://connect.mindcloud.co/v1/universal/hubflo/latest/actions/list-organizations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hubflo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hubflo/latest/actions/list-organizations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hubflo/latest/actions/list-organizations?${params}`, {
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
      "country_subscription": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "currency": "string",
      "id": "string",
      "name": "Ava Chen",
      "portal_host": "string",
      "portal_subdomain": "string",
      "project_wording": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `country_subscription` | string |  |
| `created_at` | date |  |
| `currency` | string |  |
| `id` | string |  |
| `name` | string |  |
| `portal_host` | string |  |
| `portal_subdomain` | string |  |
| `project_wording` | string |  |

## Native endpoint

Through the native Hubflo API, this operation is `GET /organizations` (base URL `https://app.hubflo.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-organizations.md) for the provider-specific parameters and requirements.

