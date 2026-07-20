# WeBeHome: Get Device Status



```
GET https://connect.mindcloud.co/v1/universal/weBeHome/latest/actions/get-device-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WeBeHome `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/weBeHome/latest/actions/get-device-status?connectionId=$CONNECTION_ID&BaseUnitID=18993" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "BaseUnitID": "18993"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/weBeHome/latest/actions/get-device-status?${params}`, {
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
| `SubUnitID` | string | no | Optional sub unit ID to return one device only. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "BUID": 1,
      "CAT": 1,
      "CD": 1,
      "DataValue": 1,
      "DESCR": "string",
      "DeviceType": "string",
      "GDESCR": "string",
      "GNO": 1,
      "LastContact": "string",
      "LastSignal": "string",
      "OperationStatus": 1,
      "ReadingUpdated": "string",
      "RSSI": 1,
      "SDESCR": "string",
      "SUID": 1,
      "Unit": "string",
      "UNO": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `BUID` | number |  |
| `CAT` | number |  |
| `CD` | number |  |
| `DataValue` | number |  |
| `DESCR` | string |  |
| `DeviceType` | string |  |
| `GDESCR` | string |  |
| `GNO` | number |  |
| `LastContact` | string |  |
| `LastSignal` | string |  |
| `OperationStatus` | number |  |
| `ReadingUpdated` | string |  |
| `RSSI` | number |  |
| `SDESCR` | string |  |
| `SUID` | number |  |
| `Unit` | string |  |
| `UNO` | number |  |

## Native endpoint

Through the native WeBeHome API, this operation is `GET WebAPI.aspx` (base URL `https://webehome.com/API`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-device-status.md) for the provider-specific parameters and requirements.

