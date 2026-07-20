# Retently: Remove Suppressed Email

Deletes a suppressed email entry from Retently.

```
DELETE https://connect.mindcloud.co/v1/universal/retently/latest/actions/remove-suppressed-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Retently `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/retently/latest/actions/remove-suppressed-email?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/retently/latest/actions/remove-suppressed-email?${params}`, {
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
| `id` | string | yes | Id |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean |  |

## Native endpoint

Through the native Retently API, this operation is `DELETE /api/v2/suppressions/emails/:id` (base URL `https://app.retently.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-suppressed-email.md) for the provider-specific parameters and requirements.

