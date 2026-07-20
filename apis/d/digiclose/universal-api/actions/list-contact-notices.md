# Digiclose: List Contact Notices



```
GET https://connect.mindcloud.co/v1/universal/digiclose/latest/actions/list-contact-notices
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Digiclose `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/digiclose/latest/actions/list-contact-notices?connectionId=$CONNECTION_ID&contactId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "contactId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/digiclose/latest/actions/list-contact-notices?${params}`, {
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
| `contactId` | number | yes | Unique identifier for the contact. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Digiclose API returns.

## Native endpoint

Through the native Digiclose API, this operation is `GET /contacts/:contact_id/notices` (base URL `https://app.digiclose.ai/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-contact-notices.md) for the provider-specific parameters and requirements.

