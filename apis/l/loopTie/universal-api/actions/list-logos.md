# Loop & Tie: List Logos

Retrieves logos for a Loop & Tie team.

```
GET https://connect.mindcloud.co/v1/universal/loopTie/latest/actions/list-logos
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Loop & Tie `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/loopTie/latest/actions/list-logos?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/loopTie/latest/actions/list-logos?${params}`, {
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
| `teamId` | string | no | The Loop & Tie team ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> | The returned logo records. |

## Native endpoint

Through the native Loop & Tie API, this operation is `GET /teams/:teamId/logos` (base URL `https://api.loopandtie.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-logos.md) for the provider-specific parameters and requirements.

