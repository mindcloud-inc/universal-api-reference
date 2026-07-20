# LEADTEX: List Contact Tags

Retrieves tags for a specific contact in LEADTEX.

```
GET https://connect.mindcloud.co/v1/universal/lEADTEX/latest/actions/list-contact-tags
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LEADTEX `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lEADTEX/latest/actions/list-contact-tags?connectionId=$CONNECTION_ID&contact_id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "contact_id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lEADTEX/latest/actions/list-contact-tags?${params}`, {
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
| `contact_id` | number | yes | ID of the contact whose tags should be returned. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        "string"
      ],
      "errors": {},
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<string> |  |
| `errors` | object |  |
| `message` | string |  |

## Native endpoint

Through the native LEADTEX API, this operation is `GET /getContactTags?api_token={{credentials.apiKey}}` (base URL `https://app.leadteh.ru/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-contact-tags.md) for the provider-specific parameters and requirements.

