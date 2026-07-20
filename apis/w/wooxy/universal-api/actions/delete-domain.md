# Wooxy: Delete Domain

Deletes an existing domain from Wooxy.

```
DELETE https://connect.mindcloud.co/v1/universal/wooxy/latest/actions/delete-domain
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wooxy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/wooxy/latest/actions/delete-domain?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wooxy/latest/actions/delete-domain?${params}`, {
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
| `domain` | string | no | The registered domain name to delete. Preferred field based on runtime verification. Example: `stage3-20260408.example.com`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `domainId` | string | no | The Wooxy domain ID to delete. Use when you already have the ID. Example: `69d68b03cab91f1ed601af02`. |
| `webHookUri` | string | no | Optional webhook URL to receive the completed domain deletion callback. Example: `https://example.com/webhooks/wooxy-domain-delete`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "result": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `result` | boolean |  |

## Native endpoint

Through the native Wooxy API, this operation is `POST v3/domain/remove` (base URL `https://api.wooxy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-domain.md) for the provider-specific parameters and requirements.

