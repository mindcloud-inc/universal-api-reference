# SuperSend: Delete Contact by Identifier

Deletes contacts from SuperSend by identifier.

```
DELETE https://connect.mindcloud.co/v1/universal/superSend/latest/actions/delete-contact-by-identifier
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SuperSend `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/superSend/latest/actions/delete-contact-by-identifier?connectionId=$CONNECTION_ID&teamId=string&campaignId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "teamId": "string",
  "campaignId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/superSend/latest/actions/delete-contact-by-identifier?${params}`, {
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
| `teamId` | string | yes |  |
| `campaignId` | string | yes |  |
| `email` | string | no | Email address to delete (required if no linkedin_url) |
| `linkedinUrl` | string | no | LinkedIn URL to delete (required if no email) |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "request_id": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |
| `request_id` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native SuperSend API, this operation is `DELETE /contacts` (base URL `https://api.supersend.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-contact-by-identifier.md) for the provider-specific parameters and requirements.

