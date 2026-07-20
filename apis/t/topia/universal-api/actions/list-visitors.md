# Topia: List Visitors

Retrieves visitors from a Topia world.

```
GET https://connect.mindcloud.co/v1/universal/topia/latest/actions/list-visitors
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Topia `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/topia/latest/actions/list-visitors?connectionId=$CONNECTION_ID&urlSlug=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "urlSlug": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/topia/latest/actions/list-visitors?${params}`, {
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
| `urlSlug` | string | yes | Topia world URL slug. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "color": "string",
      "displayName": "Ava Chen",
      "hidden": true,
      "isAdmin": true,
      "isMobile": true,
      "lastUpdate": 1,
      "moveFrom": {},
      "moveTo": {},
      "profile": {},
      "username": "Ava Chen",
      "visitorId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `color` | string |  |
| `displayName` | string |  |
| `hidden` | boolean |  |
| `isAdmin` | boolean |  |
| `isMobile` | boolean |  |
| `lastUpdate` | number |  |
| `moveFrom` | object |  |
| `moveTo` | object |  |
| `profile` | object |  |
| `username` | string |  |
| `visitorId` | number |  |

## Native endpoint

Through the native Topia API, this operation is `GET /v1/world/:urlSlug/visitors` (base URL `https://api.topia.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-visitors.md) for the provider-specific parameters and requirements.

