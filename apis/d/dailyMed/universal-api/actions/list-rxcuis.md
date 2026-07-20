# DailyMed: List RxCUIs

Retrieves RxCUIs from DailyMed.

```
GET https://connect.mindcloud.co/v1/universal/dailyMed/latest/actions/list-rxcuis
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DailyMed `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dailyMed/latest/actions/list-rxcuis?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dailyMed/latest/actions/list-rxcuis?${params}`, {
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
| `rxcui` | string | no | Unique Identifier code for an RxConcept. |
| `rxstring` | string | no | RxString value of an RxConcept. Default: `acetaminophen`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `rxtty` | string | no | RxNorm term type, such as PSN, SBD, SCD, BPCK, GPCK, or SY. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "rxcui": 1,
      "rxstring": "string",
      "rxtty": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `rxcui` | number | RxNorm Concept Unique Identifier. |
| `rxstring` | string | RxNorm string. |
| `rxtty` | string | RxNorm term type. |

## Native endpoint

Through the native DailyMed API, this operation is `GET /rxcuis.json` (base URL `https://dailymed.nlm.nih.gov/dailymed/services/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-rxcuis.md) for the provider-specific parameters and requirements.

