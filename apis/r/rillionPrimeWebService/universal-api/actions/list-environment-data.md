# Rillion Prime Web Service: List Environment Data

List configuration data for the connected Rillion Prime environment.

```
GET https://connect.mindcloud.co/v1/universal/rillionPrimeWebService/latest/actions/list-environment-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rillion Prime Web Service `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rillionPrimeWebService/latest/actions/list-environment-data?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rillionPrimeWebService/latest/actions/list-environment-data?${params}`, {
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
      "databaseName": "Ava Chen",
      "databaseServer": "string",
      "decimalsForNumber": "string",
      "decimalsForPrice": "string",
      "environment": "string",
      "languageID": "string",
      "systemCurrency": "string",
      "url": "https://example.com",
      "urlPaletteMobile": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `databaseName` | string |  |
| `databaseServer` | string |  |
| `decimalsForNumber` | string |  |
| `decimalsForPrice` | string |  |
| `environment` | string | Environment name. |
| `languageID` | string |  |
| `systemCurrency` | string | System currency code, e.g. USD. |
| `url` | string | Prime web client URL. |
| `urlPaletteMobile` | string |  |

## Native endpoint

Through the native Rillion Prime Web Service API, this operation is `POST` (base URL `{{credentials.baseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-environment-data.md) for the provider-specific parameters and requirements.

