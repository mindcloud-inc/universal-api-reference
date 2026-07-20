# Mailchimp: Set Campaign Content

Updates campaign content in Mailchimp.

```
PUT https://connect.mindcloud.co/v1/universal/mailChimp/latest/actions/set-campaign-content
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mailchimp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/mailChimp/latest/actions/set-campaign-content" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "campaign_id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mailChimp/latest/actions/set-campaign-content', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "campaign_id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `archive` | object | no |  |
| `campaign_id` | string | yes | The unique ID for the campaign. |
| `html` | string | no | HTML content. |
| `plain_text` | string | no | Plain-text content. |
| `template` | object | no |  |
| `url` | string | no |  |
| `variate_contents[]` | array<object> | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archiveHtml": "string",
      "html": "string",
      "links": {},
      "plainText": "string",
      "variateContents": [
        [
          {}
        ]
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archiveHtml` | string |  |
| `html` | string |  |
| `links` | object |  |
| `plainText` | string |  |
| `variateContents[]` | array<object> |  |

## Native endpoint

Through the native Mailchimp API, this operation is `PUT campaigns/:campaign_id/content` (base URL `https://{{credentials.serverPrefix}}.api.mailchimp.com/3.0/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/set-campaign-content.md) for the provider-specific parameters and requirements.

