# Florm: Get My Team

Retrieves your current team from Florm.

```
GET https://connect.mindcloud.co/v1/universal/florm/latest/actions/get-my-team
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Florm `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/florm/latest/actions/get-my-team?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/florm/latest/actions/get-my-team?${params}`, {
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
      "guid": "string",
      "limits": {},
      "name": "Ava Chen",
      "plan": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `guid` | string | GUID of the current Florm team. |
| `limits` | object | Current Florm team usage limits. |
| `name` | string | Name of the current Florm team. |
| `plan` | object | Current Florm team plan details. |

## Native endpoint

Through the native Florm API, this operation is `GET /v1/teams/my` (base URL `https://api.florm.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-my-team.md) for the provider-specific parameters and requirements.

