# FDIC: List Demographics Summary

Retrieves demographic banking data from FDIC.

```
GET https://connect.mindcloud.co/v1/universal/fDIC/latest/actions/list-demographics-summary
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FDIC `connectionId` ([setup](../authentication.md)).

This action also supports [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fDIC/latest/actions/list-demographics-summary?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fDIC/latest/actions/list-demographics-summary?${params}`, {
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
| `filters` | string | no | Elastic Search query string filter for demographics records. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "CBSANAME": "Ava Chen",
      "CERT": 1,
      "DIVISION": 1,
      "ID": "string",
      "OFFNDOM": 1,
      "OFFSTATE": 1,
      "OFFTOT": 1,
      "REPDTE": "string",
      "SIMS_LAT": 1,
      "SIMS_LONG": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `CBSANAME` | string |  |
| `CERT` | number |  |
| `DIVISION` | number |  |
| `ID` | string |  |
| `OFFNDOM` | number |  |
| `OFFSTATE` | number |  |
| `OFFTOT` | number |  |
| `REPDTE` | string |  |
| `SIMS_LAT` | number |  |
| `SIMS_LONG` | number |  |

## Native endpoint

Through the native FDIC API, this operation is `GET /demographics` (base URL `https://api.fdic.gov/banks`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-demographics-summary.md) for the provider-specific parameters and requirements.

