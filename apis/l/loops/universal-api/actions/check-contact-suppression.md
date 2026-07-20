# Loops: Check Contact Suppression

Retrieves contact suppression status from Loops.

```
GET https://connect.mindcloud.co/v1/universal/loops/latest/actions/check-contact-suppression
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Loops `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/loops/latest/actions/check-contact-suppression?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/loops/latest/actions/check-contact-suppression?${params}`, {
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
      "contact": {},
      "isSuppressed": true,
      "removalQuota": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contact` | object | Contact identifier payload returned by Loops. |
| `isSuppressed` | boolean | Whether the contact is suppressed. |
| `removalQuota` | object | Daily suppression-removal quota information. |

## Native endpoint

Through the native Loops API, this operation is `GET /contacts/suppression` (base URL `https://app.loops.so/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/check-contact-suppression.md) for the provider-specific parameters and requirements.

