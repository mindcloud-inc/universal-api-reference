# Dolibarr: Get Country

Retrieves a country from Dolibarr.

```
GET https://connect.mindcloud.co/v1/universal/dolibarr/latest/actions/get-country
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dolibarr `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dolibarr/latest/actions/get-country?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dolibarr/latest/actions/get-country?${params}`, {
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
| `id` | number | yes | Dolibarr country ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": 1,
      "code": "string",
      "code_iso": "string",
      "eec": "string",
      "favorite": "string",
      "id": 1,
      "label": "string",
      "numeric_code": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | number | Active flag. |
| `code` | string | Country alpha-2 code. |
| `code_iso` | string | Country alpha-3 ISO code. |
| `eec` | string | EEC flag. |
| `favorite` | string | Favorite flag. |
| `id` | number | Dolibarr country id. |
| `label` | string | Country label. |
| `numeric_code` | string | Numeric country code. |

## Native endpoint

Through the native Dolibarr API, this operation is `GET /setup/dictionary/countries/{id}` (base URL `https://mindcloud-dolibarr-0421.with7.dolicloud.com/api/index.php`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-country.md) for the provider-specific parameters and requirements.

