# WeBeHome: Get Location Status



```
GET https://connect.mindcloud.co/v1/universal/weBeHome/latest/actions/get-location-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WeBeHome `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/weBeHome/latest/actions/get-location-status?connectionId=$CONNECTION_ID&BaseUnitID=18993&ClusterID=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "BaseUnitID": "18993",
  "ClusterID": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/weBeHome/latest/actions/get-location-status?${params}`, {
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
| `BaseUnitID` | string | yes | Location ID. If 0 or omitted, the first location the user can access is used. Default: `18993`. |
| `ClusterID` | string | yes | Cluster ID for the location when BaseUnitID is supplied. Default: `1`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `SubUnitID` | string | no | Optional device ID to limit the response to one accessory. |
| `Hash` | string | no | Last hash from previous return value, empty when none was received. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ActionSets": [
        {}
      ],
      "ActiveLocation": {},
      "AddDeviceListVersion": 1,
      "Created": "string",
      "Customer": {},
      "Hash": "string",
      "LatestAppVersion": "string",
      "Locations": [
        {}
      ],
      "MenuSetting": "string",
      "ShowInMain": 1,
      "Status": 1,
      "Types": [
        {}
      ],
      "User": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ActionSets` | array<object> |  |
| `ActiveLocation` | object |  |
| `AddDeviceListVersion` | number |  |
| `Created` | string |  |
| `Customer` | object |  |
| `Hash` | string |  |
| `LatestAppVersion` | string |  |
| `Locations` | array<object> |  |
| `MenuSetting` | string |  |
| `ShowInMain` | number |  |
| `Status` | number |  |
| `Types` | array<object> |  |
| `User` | object |  |

## Native endpoint

Through the native WeBeHome API, this operation is `POST OpenAPIservice.svc/Location/GetStatus3` (base URL `https://webehome.com/API`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-location-status.md) for the provider-specific parameters and requirements.

