# LEADTEX: Detach Tag From Contact

Deletes a tag from a contact in LEADTEX by name.

```
DELETE https://connect.mindcloud.co/v1/universal/lEADTEX/latest/actions/detach-tag-from-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LEADTEX `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/lEADTEX/latest/actions/detach-tag-from-contact?connectionId=$CONNECTION_ID&contact_id=1&name=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "contact_id": "1",
  "name": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lEADTEX/latest/actions/detach-tag-from-contact?${params}`, {
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
| `contact_id` | number | yes | ID of the contact to untag. |
| `name` | string | yes | Name of the tag to detach. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "errors": {},
      "message": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |
| `errors` | object |  |
| `message` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native LEADTEX API, this operation is `POST /detachTagFromContact?api_token={{credentials.apiKey}}` (base URL `https://app.leadteh.ru/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/detach-tag-from-contact.md) for the provider-specific parameters and requirements.

