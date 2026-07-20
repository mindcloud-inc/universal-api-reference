# Festivo: List Available Countries

Retrieves available country codes from Festivo.

```
GET https://connect.mindcloud.co/v1/universal/festivo/latest/actions/list-available-countries
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Festivo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/festivo/latest/actions/list-available-countries?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/festivo/latest/actions/list-available-countries?${params}`, {
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
| `code` | string | no | Optional ISO 3166-1 alpha-2 country code filter, for example US. Example: `US`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | string | Supported ISO 3166-1 alpha-2 country code. |

## Native endpoint

Through the native Festivo API, this operation is `GET /public-holidays/countries` (base URL `https://api.getfestivo.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-available-countries.md) for the provider-specific parameters and requirements.

