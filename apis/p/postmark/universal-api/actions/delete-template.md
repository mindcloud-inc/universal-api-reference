# Postmark: Delete Template

Deletes a template from Postmark.

```
DELETE https://connect.mindcloud.co/v1/universal/postmark/latest/actions/delete-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Postmark `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/postmark/latest/actions/delete-template?connectionId=$CONNECTION_ID&templateIdOrAlias=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "templateIdOrAlias": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/postmark/latest/actions/delete-template?${params}`, {
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
| `templateIdOrAlias` | string | yes | The Postmark template ID or alias. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ErrorCode": 1,
      "Message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ErrorCode` | number |  |
| `Message` | string |  |

## Native endpoint

Through the native Postmark API, this operation is `DELETE /templates/:templateIdOrAlias` (base URL `https://api.postmarkapp.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-template.md) for the provider-specific parameters and requirements.

