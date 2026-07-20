# Bridge Interactive Platform: List lookups (OData)

Retrieves lookup records from Bridge Interactive Platform.

```
GET https://connect.mindcloud.co/v1/universal/bridgeInteractivePlatform/latest/actions/list-lookups-o-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bridge Interactive Platform `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bridgeInteractivePlatform/latest/actions/list-lookups-o-data?connectionId=$CONNECTION_ID&dataset=test" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "dataset": "test"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bridgeInteractivePlatform/latest/actions/list-lookups-o-data?${params}`, {
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

## Response

```json
{
  "success": true,
  "data": [
    {
      "LookupKey": "string",
      "LookupName": "Ava Chen",
      "LookupValue": "string",
      "ModificationTimestamp": "2026-05-07T12:00:00.000Z",
      "ResourceName": "Ava Chen",
      "StandardLookupValue": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `LookupKey` | string |  |
| `LookupName` | string |  |
| `LookupValue` | string |  |
| `ModificationTimestamp` | date |  |
| `ResourceName` | string |  |
| `StandardLookupValue` | string |  |

## Native endpoint

Through the native Bridge Interactive Platform API, this operation is `GET /OData/:dataset/Lookup` (base URL `https://api.bridgedataoutput.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-lookups-o-data.md) for the provider-specific parameters and requirements.

