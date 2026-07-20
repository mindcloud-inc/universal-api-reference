# Mailchimp: Get Campaign Content

Retrieves campaign content from Mailchimp.

```
GET https://connect.mindcloud.co/v1/universal/mailChimp/latest/actions/get-campaign-content
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mailchimp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mailChimp/latest/actions/get-campaign-content?connectionId=$CONNECTION_ID&campaign_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "campaign_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mailChimp/latest/actions/get-campaign-content?${params}`, {
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
| `campaign_id` | string | yes | The unique ID for the campaign. |
| `exclude_fields` | string | no |  |
| `fields` | string | no |  |

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

Through the native Mailchimp API, this operation is `GET campaigns/:campaign_id/content` (base URL `https://{{credentials.serverPrefix}}.api.mailchimp.com/3.0/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-campaign-content.md) for the provider-specific parameters and requirements.

