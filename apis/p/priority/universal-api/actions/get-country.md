# Priority: Get Country

Retrieves a country from Priority.

```
GET https://connect.mindcloud.co/v1/universal/priority/latest/actions/get-country
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Priority `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/priority/latest/actions/get-country?connectionId=$CONNECTION_ID&countryName=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "countryName": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/priority/latest/actions/get-country?${params}`, {
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
| `countryName` | string | yes | Priority country key. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "COUNTRYCODE": "string",
      "COUNTRYCODE3": "string",
      "COUNTRYNAME": "Ava Chen",
      "EEAFLAG": "string",
      "NATIONALITY": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `COUNTRYCODE` | string |  |
| `COUNTRYCODE3` | string |  |
| `COUNTRYNAME` | string |  |
| `EEAFLAG` | string |  |
| `NATIONALITY` | string |  |

## Native endpoint

Through the native Priority API, this operation is `GET /COUNTRIES(COUNTRYNAME=':countryName')` (base URL `https://t.eu.priority-connect.online/odata/Priority/tabbtd38.ini/usdemo`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-country.md) for the provider-specific parameters and requirements.

