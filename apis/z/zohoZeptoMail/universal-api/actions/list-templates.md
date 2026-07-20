# Zoho ZeptoMail: List Templates

Retrieves email templates from Zoho ZeptoMail.

```
GET https://connect.mindcloud.co/v1/universal/zohoZeptoMail/latest/actions/list-templates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho ZeptoMail `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoZeptoMail/latest/actions/list-templates?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoZeptoMail/latest/actions/list-templates?${params}`, {
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
| `limit` | number | no | Maximum number of templates to return. |
| `offset` | number | no | Offset of the first template to return. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {
          "created_time": "2026-05-07T12:00:00.000Z",
          "description": "string",
          "modified_time": "2026-05-07T12:00:00.000Z",
          "template_alias": "string",
          "template_key": "string",
          "template_name": "Ava Chen"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data[].created_time` | date |  |
| `data[].description` | string |  |
| `data[].modified_time` | date |  |
| `data[].template_alias` | string |  |
| `data[].template_key` | string |  |
| `data[].template_name` | string |  |

## Native endpoint

Through the native Zoho ZeptoMail API, this operation is `GET agents/:agentAlias/templates` (base URL `https://api.zeptomail.com/v1.1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-templates.md) for the provider-specific parameters and requirements.

