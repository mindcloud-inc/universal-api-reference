# OpenPLZ: List German Federal States



```
GET https://connect.mindcloud.co/v1/universal/openPLZ/latest/actions/list-german-federal-states
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OpenPLZ `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openPLZ/latest/actions/list-german-federal-states?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openPLZ/latest/actions/list-german-federal-states?${params}`, {
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
      "key": "string",
      "name": "Ava Chen",
      "seatOfGovernment": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `key` | string |  |
| `name` | string |  |
| `seatOfGovernment` | string |  |

## Native endpoint

Through the native OpenPLZ API, this operation is `GET /de/FederalStates` (base URL `https://openplzapi.org`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-german-federal-states.md) for the provider-specific parameters and requirements.

