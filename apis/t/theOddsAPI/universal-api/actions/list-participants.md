# The Odds: List Participants

Retrieves participants for a sport from The Odds API.

```
GET https://connect.mindcloud.co/v1/universal/theOddsAPI/latest/actions/list-participants
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a The Odds `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/theOddsAPI/latest/actions/list-participants?connectionId=$CONNECTION_ID&sport=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "sport": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/theOddsAPI/latest/actions/list-participants?${params}`, {
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
| `sport` | string | yes | The sport key returned by List Sports. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "full_name": "Ava Chen",
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `full_name` | string |  |
| `id` | string |  |

## Native endpoint

Through the native The Odds API, this operation is `GET /v4/sports/:sport/participants` (base URL `https://api.the-odds-api.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-participants.md) for the provider-specific parameters and requirements.

