# Smsmobileapi: List Connected Mobiles

Retrieves connected gateway mobiles from Smsmobileapi.

```
GET https://connect.mindcloud.co/v1/universal/smsmobileapi/latest/actions/list-connected-mobiles
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Smsmobileapi `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smsmobileapi/latest/actions/list-connected-mobiles?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smsmobileapi/latest/actions/list-connected-mobiles?${params}`, {
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
| `sid` | string | no | Filter the result to one exact connected mobile SID. |
| `search` | string | no | Search connected mobile fields such as SID, date, battery, version, or label. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "connected_available": 1,
      "connected_limit": 1,
      "connected_now": 1,
      "filters": {},
      "items": [
        {}
      ],
      "note": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `connected_available` | number | Remaining mobile connection slots available. |
| `connected_limit` | number | Maximum number of connected mobiles allowed for the account. |
| `connected_now` | number | Number of mobiles currently connected. |
| `filters` | object | Echoed filter values applied to the request. |
| `items` | array<object> | Connected mobile records returned by the gateway. |
| `note` | string | Provider note about gateway-mobile statistics availability. |
| `success` | boolean | Whether the gateway-mobile lookup succeeded. |

## Native endpoint

Through the native Smsmobileapi API, this operation is `GET /gateway/mobile/list/` (base URL `https://api.smsmobileapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-connected-mobiles.md) for the provider-specific parameters and requirements.

