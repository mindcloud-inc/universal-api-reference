# OpenPLZ: List German Districts by Federal State



```
GET https://connect.mindcloud.co/v1/universal/openPLZ/latest/actions/list-german-districts-by-federal-state
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OpenPLZ `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openPLZ/latest/actions/list-german-districts-by-federal-state?connectionId=$CONNECTION_ID&limit=25&offset=0&key=09" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "key": "09"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openPLZ/latest/actions/list-german-districts-by-federal-state?${params}`, {
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
| `key` | string | yes | German federal state key, such as 09 for Bavaria. Default: `09`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "administrativeHeadquarters": "string",
      "federalState": {},
      "governmentRegion": {},
      "key": "string",
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
| `administrativeHeadquarters` | string |  |
| `federalState` | object |  |
| `governmentRegion` | object |  |
| `key` | string |  |
| `name` | string |  |
| `type` | string |  |

## Native endpoint

Through the native OpenPLZ API, this operation is `GET /de/FederalStates/{key}/Districts` (base URL `https://openplzapi.org`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-german-districts-by-federal-state.md) for the provider-specific parameters and requirements.

