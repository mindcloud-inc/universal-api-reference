# WeBeHome: Get Base Unit Configuration



```
GET https://connect.mindcloud.co/v1/universal/weBeHome/latest/actions/get-base-unit-configuration
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WeBeHome `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/weBeHome/latest/actions/get-base-unit-configuration?connectionId=$CONNECTION_ID&BaseUnitID=18993" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "BaseUnitID": "18993"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/weBeHome/latest/actions/get-base-unit-configuration?${params}`, {
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
| `BaseUnitID` | string | yes | Base unit ID. Leave empty to return all base units the user can access. Default: `18993`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "BUID": 1,
      "CAT": 1,
      "DESCR": "string",
      "GDESCR": "string",
      "GNO": 1,
      "SDESCR": "string",
      "SUID": 1,
      "SUTID": 1,
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
| `DESCR` | string |  |
| `GDESCR` | string |  |
| `GNO` | number |  |
| `SDESCR` | string |  |
| `SUID` | number |  |
| `SUTID` | number |  |
| `UNO` | number |  |

## Native endpoint

Through the native WeBeHome API, this operation is `GET WebAPI.aspx` (base URL `https://webehome.com/API`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-base-unit-configuration.md) for the provider-specific parameters and requirements.

