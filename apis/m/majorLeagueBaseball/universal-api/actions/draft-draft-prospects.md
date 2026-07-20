# Major League Baseball: View MLB Draft Prospects



```
GET https://connect.mindcloud.co/v1/universal/majorLeagueBaseball/latest/actions/draft-draft-prospects
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Major League Baseball `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/majorLeagueBaseball/latest/actions/draft-draft-prospects?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/majorLeagueBaseball/latest/actions/draft-draft-prospects?${params}`, {
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
      "person": "string",
      "pickNumber": "string",
      "round": "string",
      "year": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `person` | string |  |
| `pickNumber` | string |  |
| `round` | string |  |
| `year` | string |  |

## Native endpoint

Through the native Major League Baseball API, this operation is `GET /v1/draft/prospects/{year}` (base URL `https://statsapi.mlb.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/draft-draft-prospects.md) for the provider-specific parameters and requirements.

