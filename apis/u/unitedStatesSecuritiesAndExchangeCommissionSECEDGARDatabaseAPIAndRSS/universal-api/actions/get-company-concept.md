# United States Securities and Exchange Commission (SEC) EDGAR Database: Get Company Concept

Retrieves company concept facts from SEC EDGAR.

```
GET https://connect.mindcloud.co/v1/universal/unitedStatesSecuritiesAndExchangeCommissionSECEDGARDatabaseAPIAndRSS/latest/actions/get-company-concept
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a United States Securities and Exchange Commission (SEC) EDGAR Database `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/unitedStatesSecuritiesAndExchangeCommissionSECEDGARDatabaseAPIAndRSS/latest/actions/get-company-concept?connectionId=$CONNECTION_ID&cik=0000320193&taxonomy=us-gaap&tag=AccountsPayableCurrent" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "cik": "0000320193",
  "taxonomy": "us-gaap",
  "tag": "AccountsPayableCurrent"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/unitedStatesSecuritiesAndExchangeCommissionSECEDGARDatabaseAPIAndRSS/latest/actions/get-company-concept?${params}`, {
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
| `cik` | string | yes | Zero-padded 10-digit Central Index Key. Example: `0000320193`. |
| `taxonomy` | string | yes | Taxonomy namespace, such as us-gaap, ifrs-full, dei, or srt. Example: `us-gaap`. |
| `tag` | string | yes | Taxonomy tag, such as AccountsPayableCurrent. Example: `AccountsPayableCurrent`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cik": 1,
      "description": "string",
      "entityName": "Ava Chen",
      "label": "string",
      "tag": "string",
      "taxonomy": "string",
      "units": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cik` | number | Central Index Key as returned by SEC. |
| `description` | string | Concept description. |
| `entityName` | string | Registrant name. |
| `label` | string | Concept label. |
| `tag` | string | Taxonomy tag. |
| `taxonomy` | string | Taxonomy namespace. |
| `units` | object | Fact arrays grouped by unit. |

## Native endpoint

Through the native United States Securities and Exchange Commission (SEC) EDGAR Database API, this operation is `GET https://data.sec.gov/api/xbrl/companyconcept/CIK[:cik]/[:taxonomy]/[:tag].json` (base URL `https://www.sec.gov`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-company-concept.md) for the provider-specific parameters and requirements.

