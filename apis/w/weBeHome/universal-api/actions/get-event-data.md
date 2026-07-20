# WeBeHome: Get Event Data



```
GET https://connect.mindcloud.co/v1/universal/weBeHome/latest/actions/get-event-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WeBeHome `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/weBeHome/latest/actions/get-event-data?connectionId=$CONNECTION_ID&BaseUnitID=18993&LastDataID=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "BaseUnitID": "18993",
  "LastDataID": "0"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/weBeHome/latest/actions/get-event-data?${params}`, {
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
| `BaseUnitID` | string | yes | Base unit ID. Leave empty to search all accessible base units. Default: `18993`. |
| `LastDataID` | string | yes | Start returning rows after this data ID. Empty means the last 24 hours. Default: `0`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "BUID": 1,
      "DID": 1,
      "DT": "string",
      "DV": 1,
      "EID": 1,
      "OS": 1,
      "SUID": 1,
      "UID": 1
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
| `DV` | number |  |
| `EID` | number |  |
| `OS` | number |  |
| `SUID` | number |  |
| `UID` | number |  |

## Native endpoint

Through the native WeBeHome API, this operation is `GET WebAPI.aspx` (base URL `https://webehome.com/API`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-event-data.md) for the provider-specific parameters and requirements.

