# Goodbarber eCommerce: List App Global Downloads



```
GET https://connect.mindcloud.co/v1/universal/goodbarberECommerce/latest/actions/list-app-global-downloads
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Goodbarber eCommerce `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/goodbarberECommerce/latest/actions/list-app-global-downloads?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/goodbarberECommerce/latest/actions/list-app-global-downloads?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `platform` | string | no | Target platform. Defaults to "all". |

## Response

```json
{
  "success": true,
  "data": [
    {
      "total_global_downloads": 1,
      "versions": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `total_global_downloads` | number | <div class="field_description">Total number of app downloads on the platform.</div> |
| `versions` | array<object> | <div class="field_description">Distribution of downloads across the specified platform's versions.</div> |

## Native endpoint

Through the native Goodbarber eCommerce API, this operation is `GET /publicapi/v2/general/stats/:webzine_id/downloads_global/` (base URL `https://commerce.goodbarber.dev`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-app-global-downloads.md) for the provider-specific parameters and requirements.

