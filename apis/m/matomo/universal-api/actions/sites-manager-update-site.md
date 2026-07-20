# Matomo: SitesManager update Site



```
PUT https://connect.mindcloud.co/v1/universal/matomo/latest/actions/sites-manager-update-site
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Matomo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/matomo/latest/actions/sites-manager-update-site" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "idSite": "1"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/matomo/latest/actions/sites-manager-update-site', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "idSite": "1"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `idSite` | number | yes | Matomo API parameter. Default: `1`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `siteName` | string | no | Matomo API parameter. |
| `urls` | string | no | Matomo API parameter. |
| `ecommerce` | string | no | Matomo API parameter. |
| `siteSearch` | string | no | Matomo API parameter. |
| `searchKeywordParameters` | string | no | Matomo API parameter. |
| `searchCategoryParameters` | string | no | Matomo API parameter. |
| `excludedIps` | string | no | Matomo API parameter. |
| `excludedQueryParameters` | string | no | Matomo API parameter. |
| `timezone` | string | no | Matomo API parameter. |
| `currency` | string | no | Matomo API parameter. |
| `group` | string | no | Matomo API parameter. |
| `startDate` | string | no | Matomo API parameter. |
| `excludedUserAgents` | string | no | Matomo API parameter. |
| `keepURLFragments` | string | no | Matomo API parameter. |
| `type` | string | no | Matomo API parameter. |
| `settingValues` | string | no | Matomo API parameter. |
| `excludeUnknownUrls` | string | no | Matomo API parameter. |
| `excludedReferrers` | string | no | Matomo API parameter. |

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

Through the native Matomo API, this operation is `POST /index.php` (base URL `https://mindcloud.matomo.cloud`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/sites-manager-update-site.md) for the provider-specific parameters and requirements.

