# DailyMed: List Drug Classes

Retrieves drug classes from DailyMed.

```
GET https://connect.mindcloud.co/v1/universal/dailyMed/latest/actions/list-drug-classes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DailyMed `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dailyMed/latest/actions/list-drug-classes?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dailyMed/latest/actions/list-drug-classes?${params}`, {
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
| `className` | string | no | Name of the drug class. |
| `drugClassCode` | string | no | Pharmacologic drug class code. |
| `uniiCode` | string | no | Unique Ingredient Identifier code. Default: `R16CO5Y76E`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `drugClassCodingSystem` | string | no | Coding system for the drug class code. |
| `classCodeType` | string | no | Drug class type: all, epc, moa, pe, or ci. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": "string",
      "codingSystem": "string",
      "name": "Ava Chen",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | string | Drug class code. |
| `codingSystem` | string | Coding system for the drug class code. |
| `name` | string | Drug class name. |
| `type` | string | Drug class type. |

## Native endpoint

Through the native DailyMed API, this operation is `GET /drugclasses.json` (base URL `https://dailymed.nlm.nih.gov/dailymed/services/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-drug-classes.md) for the provider-specific parameters and requirements.

