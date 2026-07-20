# Podscan: Get Team Alert

Retrieves a team alert from Podscan.

```
GET https://connect.mindcloud.co/v1/universal/podscan/latest/actions/get-team-alert
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Podscan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/podscan/latest/actions/get-team-alert?connectionId=$CONNECTION_ID&alert=string&team=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "alert": "string",
  "team": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/podscan/latest/actions/get-team-alert?${params}`, {
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
| `alert` | string | yes | The alert ID. |
| `team` | string | yes | The team ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "alert": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `alert` | object |  |

## Native endpoint

Through the native Podscan API, this operation is `GET /teams/{team}/alerts/{alert}` (base URL `https://podscan.fm/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-team-alert.md) for the provider-specific parameters and requirements.

