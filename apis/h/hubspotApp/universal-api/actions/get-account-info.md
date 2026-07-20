# HubSpot: Get Account Info

Retrieves account details from HubSpot.

```
GET https://connect.mindcloud.co/v1/universal/hubspotApp/latest/actions/get-account-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HubSpot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hubspotApp/latest/actions/get-account-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hubspotApp/latest/actions/get-account-info?${params}`, {
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
      "accountType": "string",
      "additionalCurrencies": [
        {}
      ],
      "companyCurrency": "string",
      "dataHostingLocation": "string",
      "portalId": 1,
      "timeZone": "string",
      "uiDomain": "string",
      "utcOffset": "string",
      "utcOffsetMilliseconds": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountType` | string | The HubSpot account type. |
| `additionalCurrencies` | array<object> | Additional currencies configured for the account. |
| `companyCurrency` | string | The default company currency code. |
| `dataHostingLocation` | string | The data hosting region for the account. |
| `portalId` | number | The HubSpot portal ID. |
| `timeZone` | string | The default account time zone. |
| `uiDomain` | string | The HubSpot app domain for the account. |
| `utcOffset` | string | The account UTC offset. |
| `utcOffsetMilliseconds` | number | The account UTC offset in milliseconds. |

## Native endpoint

Through the native HubSpot API, this operation is `GET account-info/v3/details` (base URL `https://api.hubapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-account-info.md) for the provider-specific parameters and requirements.

