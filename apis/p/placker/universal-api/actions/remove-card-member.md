# Placker: Remove Card Member



```
DELETE https://connect.mindcloud.co/v1/universal/placker/latest/actions/remove-card-member
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Placker `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/placker/latest/actions/remove-card-member?connectionId=$CONNECTION_ID&card=12345&member=987" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "card": "12345",
  "member": "987"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/placker/latest/actions/remove-card-member?${params}`, {
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
| `card` | number | yes | Card ID. Example: `12345`. |
| `member` | number | yes | Member ID. Example: `987`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Placker API returns.

## Native endpoint

Through the native Placker API, this operation is `DELETE /card/:card/member/:member` (base URL `https://api.placker.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-card-member.md) for the provider-specific parameters and requirements.

