# United States Securities and Exchange Commission (SEC) EDGAR Database: Get Company Facts

Retrieves company XBRL facts from SEC EDGAR.

```
GET https://connect.mindcloud.co/v1/universal/unitedStatesSecuritiesAndExchangeCommissionSECEDGARDatabaseAPIAndRSS/latest/actions/get-company-facts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a United States Securities and Exchange Commission (SEC) EDGAR Database `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/unitedStatesSecuritiesAndExchangeCommissionSECEDGARDatabaseAPIAndRSS/latest/actions/get-company-facts?connectionId=$CONNECTION_ID&cik=0000320193" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "cik": "0000320193"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/unitedStatesSecuritiesAndExchangeCommissionSECEDGARDatabaseAPIAndRSS/latest/actions/get-company-facts?${params}`, {
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
| `cik` | string | yes | Zero-padded 10-digit Central Index Key, such as 0000320193 for Apple. Example: `0000320193`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cik": 1,
      "entityName": "Ava Chen",
      "facts": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cik` | number | Central Index Key as returned by SEC. |
| `entityName` | string | Registrant name. |
| `facts` | object | XBRL fact data grouped by taxonomy and tag. |

## Native endpoint

Through the native United States Securities and Exchange Commission (SEC) EDGAR Database API, this operation is `GET https://data.sec.gov/api/xbrl/companyfacts/CIK[:cik].json` (base URL `https://www.sec.gov`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-company-facts.md) for the provider-specific parameters and requirements.

