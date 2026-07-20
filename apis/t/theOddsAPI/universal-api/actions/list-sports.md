# The Odds: List Sports

Retrieves supported sports from The Odds API.

```
GET https://connect.mindcloud.co/v1/universal/theOddsAPI/latest/actions/list-sports
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a The Odds `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/theOddsAPI/latest/actions/list-sports?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/theOddsAPI/latest/actions/list-sports?${params}`, {
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
| `all` | boolean | no | Set true to include both in-season and out-of-season sports. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "description": "string",
      "group": "string",
      "has_outrights": true,
      "key": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `description` | string |  |
| `group` | string |  |
| `has_outrights` | boolean |  |
| `key` | string |  |
| `title` | string |  |

## Native endpoint

Through the native The Odds API, this operation is `GET /v4/sports/` (base URL `https://api.the-odds-api.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-sports.md) for the provider-specific parameters and requirements.

