# KeyVox: List Units

Lists rooms and devices in your KeyVox account.

```
GET https://connect.mindcloud.co/v1/universal/keyVox/latest/actions/list-units
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a KeyVox `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/keyVox/latest/actions/list-units?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/keyVox/latest/actions/list-units?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "placeName": "Ava Chen",
      "placeType": "string",
      "unitId": "string",
      "unitName": "Ava Chen",
      "unitState": "string",
      "unitType": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `placeName` | string | Name of the place that owns the unit. |
| `placeType` | string | Type of place associated with the unit. |
| `unitId` | string | Unique KeyVox unit identifier. |
| `unitName` | string | Human-readable unit name. |
| `unitState` | string | Current unit state code returned by KeyVox. |
| `unitType` | string | Unit type label. |

## Native endpoint

Through the native KeyVox API, this operation is `POST /v1/getUnits` (base URL `https://eco.blockchainlock.io/api/eagle-pms`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-units.md) for the provider-specific parameters and requirements.

