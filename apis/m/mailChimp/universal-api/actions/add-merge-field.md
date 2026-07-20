# Mailchimp: Add Merge Field

Creates a new merge field in a Mailchimp audience.

```
POST https://connect.mindcloud.co/v1/universal/mailChimp/latest/actions/add-merge-field
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mailchimp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/mailChimp/latest/actions/add-merge-field" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "list_id": "string",
  "name": "Ava Chen",
  "type": "address"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mailChimp/latest/actions/add-merge-field', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "list_id": "string",
    "name": "Ava Chen",
    "type": "address"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `default_value` | string | no |  |
| `display_order` | number | no |  |
| `help_text` | string | no |  |
| `list_id` | string | yes | The unique ID for the Mailchimp audience. |
| `name` | string | yes | Merge field name. |
| `options` | object | no |  |
| `public` | boolean | no |  |
| `required` | boolean | no |  |
| `tag` | string | no | Merge field tag. |
| `type` | list<string> | yes | Merge field type. One of: `address`, `birthday`, `date`, `dropdown`, `imageurl`, `number`, `phone`, `radio`, `text`, `url`, `zip`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "displayOrder": 1,
      "helpText": "string",
      "listId": "string",
      "mergeId": 1,
      "name": "Ava Chen",
      "required": true,
      "tag": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `displayOrder` | number |  |
| `helpText` | string |  |
| `listId` | string |  |
| `mergeId` | number |  |
| `name` | string |  |
| `required` | boolean |  |
| `tag` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Mailchimp API, this operation is `POST lists/:list_id/merge-fields` (base URL `https://{{credentials.serverPrefix}}.api.mailchimp.com/3.0/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-merge-field.md) for the provider-specific parameters and requirements.

