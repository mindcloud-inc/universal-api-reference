# Goodbarber eCommerce: List App Downloads



```
GET https://connect.mindcloud.co/v1/universal/goodbarberECommerce/latest/actions/list-app-downloads
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Goodbarber eCommerce `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/goodbarberECommerce/latest/actions/list-app-downloads?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/goodbarberECommerce/latest/actions/list-app-downloads?${params}`, {
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
| `endDate` | string | no | End date (included) with format %Y-%m-%d . Defaults to yesterday. |
| `platform` | string | no | Target platform. Defaults to "all". |
| `startDate` | string | no | Start date (included) with format %Y-%m-%d . Defaults to one month ago. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "history": [
        {}
      ],
      "total_downloads": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `history` | array<object> | <div class="field_description">History of downloads per day.</div> |
| `total_downloads` | number | <div class="field_description">Total number of app downloads during the specified time interval.</div> |

## Native endpoint

Through the native Goodbarber eCommerce API, this operation is `GET /publicapi/v2/general/stats/:webzine_id/downloads/` (base URL `https://commerce.goodbarber.dev`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-app-downloads.md) for the provider-specific parameters and requirements.

