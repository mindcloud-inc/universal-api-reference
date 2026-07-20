# Mailchimp: Get Template

Retrieves a template from Mailchimp.

```
GET https://connect.mindcloud.co/v1/universal/mailChimp/latest/actions/get-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mailchimp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mailChimp/latest/actions/get-template?connectionId=$CONNECTION_ID&template_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "template_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mailChimp/latest/actions/get-template?${params}`, {
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
| `exclude_fields` | string | no |  |
| `fields` | string | no |  |
| `template_id` | string | yes | The unique ID for the template. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "category": "string",
      "contentType": "string",
      "createdBy": "string",
      "dateCreated": "string",
      "dateEdited": "string",
      "dragAndDrop": true,
      "editedBy": "string",
      "id": 1,
      "links": [
        [
          {}
        ]
      ],
      "name": "Ava Chen",
      "responsive": true,
      "shareUrl": "https://example.com",
      "thumbnail": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `category` | string |  |
| `contentType` | string |  |
| `createdBy` | string |  |
| `dateCreated` | string |  |
| `dateEdited` | string |  |
| `dragAndDrop` | boolean |  |
| `editedBy` | string |  |
| `id` | number |  |
| `links[]` | array<object> |  |
| `links[].href` | string |  |
| `links[].method` | string |  |
| `links[].rel` | string |  |
| `links[].targetSchema` | string |  |
| `name` | string |  |
| `responsive` | boolean |  |
| `shareUrl` | string |  |
| `thumbnail` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Mailchimp API, this operation is `GET templates/:template_id` (base URL `https://{{credentials.serverPrefix}}.api.mailchimp.com/3.0/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-template.md) for the provider-specific parameters and requirements.

