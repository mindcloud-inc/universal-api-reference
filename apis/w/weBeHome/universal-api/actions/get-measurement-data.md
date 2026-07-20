# WeBeHome: Get Measurement Data



```
GET https://connect.mindcloud.co/v1/universal/weBeHome/latest/actions/get-measurement-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WeBeHome `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/weBeHome/latest/actions/get-measurement-data?connectionId=$CONNECTION_ID&BaseUnitID=18993&FromDT=2026-04-09" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "BaseUnitID": "18993",
  "FromDT": "2026-04-09"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/weBeHome/latest/actions/get-measurement-data?${params}`, {
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
| `SubUnitID` | string | no | One ID, a comma-separated list of IDs, or empty. |
| `BaseUnitID` | string | yes | Base unit ID. Default: `18993`. |
| `FromDT` | string | yes | Start date in yyyy-mm-dd. Empty means the last 7 days. Default: `2026-04-09`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "BUID": 1,
      "DID": 1,
      "DT": "string",
      "SUID": 1,
      "VAL": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `BUID` | number |  |
| `DID` | number |  |
| `DT` | string |  |
| `SUID` | number |  |
| `VAL` | number |  |

## Native endpoint

Through the native WeBeHome API, this operation is `GET WebAPI.aspx` (base URL `https://webehome.com/API`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-measurement-data.md) for the provider-specific parameters and requirements.

