# DailyMed: List UNIIs

Retrieves UNIIs from DailyMed.

```
GET https://connect.mindcloud.co/v1/universal/dailyMed/latest/actions/list-uniis
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DailyMed `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dailyMed/latest/actions/list-uniis?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dailyMed/latest/actions/list-uniis?${params}`, {
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
| `uniiCode` | string | no | Unique Ingredient Identifier code. |
| `activeMoiety` | string | no | Active moiety related to a UNII code. Default: `ASPIRIN`. |
| `rxcui` | string | no | RxNorm Concept Unique Identifier code. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `drugClassCode` | string | no | Pharmacologic drug class code. |
| `drugClassCodingSystem` | string | no | Coding system for the drug class code. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active_moiety": "string",
      "unii_code": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active_moiety` | string | Active moiety related to the UNII. |
| `unii_code` | string | Unique Ingredient Identifier code. |

## Native endpoint

Through the native DailyMed API, this operation is `GET /uniis.json` (base URL `https://dailymed.nlm.nih.gov/dailymed/services/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-uniis.md) for the provider-specific parameters and requirements.

