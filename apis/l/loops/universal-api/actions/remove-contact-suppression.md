# Loops: Remove Contact Suppression

Deletes contact suppression from Loops by email or user ID.

```
DELETE https://connect.mindcloud.co/v1/universal/loops/latest/actions/remove-contact-suppression
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Loops `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/loops/latest/actions/remove-contact-suppression?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/loops/latest/actions/remove-contact-suppression?${params}`, {
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
| `email` | string | no |  |
| `userId` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "removalQuota": {},
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string | Provider status message for the suppression-removal attempt. |
| `removalQuota` | object | Daily suppression-removal quota information returned by Loops. |
| `success` | boolean | Whether Loops removed the suppression entry. |

## Native endpoint

Through the native Loops API, this operation is `DELETE /contacts/suppression` (base URL `https://app.loops.so/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-contact-suppression.md) for the provider-specific parameters and requirements.

