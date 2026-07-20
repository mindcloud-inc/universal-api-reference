# Matomo: SitesManager get Sites With Minimum Access



```
GET https://connect.mindcloud.co/v1/universal/matomo/latest/actions/sites-manager-get-sites-with-minimum-access
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Matomo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/matomo/latest/actions/sites-manager-get-sites-with-minimum-access?connectionId=$CONNECTION_ID&permission=string&%3Fstring%20pattern=string&%3Fint%20limit=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "permission": "string",
  "?string pattern": "string",
  "?int limit": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/matomo/latest/actions/sites-manager-get-sites-with-minimum-access?${params}`, {
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
| `permission` | string | yes | Matomo API parameter. |
| `?string pattern` | string | yes | Matomo API parameter. |
| `?int limit` | string | yes | Matomo API parameter. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `sitesToExclude` | string | no | Matomo API parameter. Default: `Array`. |
| `siteTypesToExclude` | string | no | Matomo API parameter. Default: `Array`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "label": "string",
      "nb_actions": 1,
      "nb_visits": 1,
      "result": "string",
      "value": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `label` | string | Matomo response label |
| `nb_actions` | number | Actions |
| `nb_visits` | number | Visits |
| `result` | string | Operation result |
| `value` | string | Matomo response value |

## Native endpoint

Through the native Matomo API, this operation is `POST /index.php` (base URL `https://mindcloud.matomo.cloud`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/sites-manager-get-sites-with-minimum-access.md) for the provider-specific parameters and requirements.

