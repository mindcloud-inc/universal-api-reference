# Bridge Interactive Platform: Get office (OData)

Retrieves an office from Bridge Interactive Platform.

```
GET https://connect.mindcloud.co/v1/universal/bridgeInteractivePlatform/latest/actions/get-office-o-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bridge Interactive Platform `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bridgeInteractivePlatform/latest/actions/get-office-o-data?connectionId=$CONNECTION_ID&dataset=test&OfficeKey=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "dataset": "test",
  "OfficeKey": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bridgeInteractivePlatform/latest/actions/get-office-o-data?${params}`, {
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
| `dataset` | string | yes | Bridge dataset code. This tenant was validated against dataset test. Default: `test`. |
| `OfficeKey` | string | yes | OData office identifier from Bridge. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "OfficeEmail": "ava@example.com",
      "OfficeKey": "string",
      "OfficeMlsId": "string",
      "OfficeName": "Ava Chen",
      "OfficeStatus": "string",
      "OfficeType": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `OfficeEmail` | string |  |
| `OfficeKey` | string |  |
| `OfficeMlsId` | string |  |
| `OfficeName` | string |  |
| `OfficeStatus` | string |  |
| `OfficeType` | string |  |

## Native endpoint

Through the native Bridge Interactive Platform API, this operation is `GET /OData/:dataset/Office(':OfficeKey')` (base URL `https://api.bridgedataoutput.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-office-o-data.md) for the provider-specific parameters and requirements.

