# Loopy Loyalty: Campaign Exists By Name



```
GET https://connect.mindcloud.co/v1/universal/loopyLoyalty/latest/actions/campaign-exists-by-name
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Loopy Loyalty `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/loopyLoyalty/latest/actions/campaign-exists-by-name?connectionId=$CONNECTION_ID&name=Codex%20Stage3%20Campaign%201" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "name": "Codex Stage3 Campaign 1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/loopyLoyalty/latest/actions/campaign-exists-by-name?${params}`, {
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
| `name` | string | yes | Campaign name to check. Example: `Codex Stage3 Campaign 1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "exists": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `exists` | boolean | Whether a campaign with the supplied name exists. |

## Native endpoint

Through the native Loopy Loyalty API, this operation is `GET /campaign/exists/:name` (base URL `https://api.loopyloyalty.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/campaign-exists-by-name.md) for the provider-specific parameters and requirements.

