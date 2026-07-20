# GMass: Remove Unsubscribed Domain

Deletes an unsubscribed domain from GMass.

```
DELETE https://connect.mindcloud.co/v1/universal/gMass/latest/actions/remove-unsubscribed-domain
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GMass `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/gMass/latest/actions/remove-unsubscribed-domain?connectionId=$CONNECTION_ID&domain=codex-stage3.invalid" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "domain": "codex-stage3.invalid"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gMass/latest/actions/remove-unsubscribed-domain?${params}`, {
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
| `domain` | string | yes | Domain to remove from the account unsubscribe domain list. Example: `codex-stage3.invalid`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "domain": "string",
      "unsubscribeTime": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `domain` | string | Domain removed from the account unsubscribe domain list. |
| `unsubscribeTime` | date | Time on the unsubscribe domain record returned by GMass. |

## Native endpoint

Through the native GMass API, this operation is `DELETE /unsubscribes/domain/:domain` (base URL `https://api.gmass.co/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-unsubscribed-domain.md) for the provider-specific parameters and requirements.

