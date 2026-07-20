# Maildrip: Atomically create a contact group and attach it to an opt-in page



```
POST https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/atomically-create-a-contact-group-and-attach-it-to-an-opt-in-page
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Maildrip `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/atomically-create-a-contact-group-and-attach-it-to-an-opt-in-page" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "pageId": "string",
  "title": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/atomically-create-a-contact-group-and-attach-it-to-an-opt-in-page', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "pageId": "string",
    "title": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `pageId` | string | yes |  |
| `title` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string | Group created and linked to the opt-in page |

## Native endpoint

Through the native Maildrip API, this operation is `POST /api/v1/opt-in-pages/{pageId}/groups` (base URL `https://api.maildrip.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/atomically-create-a-contact-group-and-attach-it-to-an-opt-in-page.md) for the provider-specific parameters and requirements.

