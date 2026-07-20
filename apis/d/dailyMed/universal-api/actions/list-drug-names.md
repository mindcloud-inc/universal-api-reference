# DailyMed: List Drug Names

Retrieves drug names from DailyMed.

```
GET https://connect.mindcloud.co/v1/universal/dailyMed/latest/actions/list-drug-names
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DailyMed `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dailyMed/latest/actions/list-drug-names?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dailyMed/latest/actions/list-drug-names?${params}`, {
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
| `drugName` | string | no | Generic or brand name of the drug. Default: `acetaminophen`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `nameType` | string | no | Whether the drug name is generic, brand, or both. |
| `manufacturer` | string | no | Name of manufacturer for the drug. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "drug_name": "Ava Chen",
      "name_type": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `drug_name` | string | Drug generic or brand name. |
| `name_type` | string | Name type, such as G for generic or B for brand. |

## Native endpoint

Through the native DailyMed API, this operation is `GET /drugnames.json` (base URL `https://dailymed.nlm.nih.gov/dailymed/services/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-drug-names.md) for the provider-specific parameters and requirements.

