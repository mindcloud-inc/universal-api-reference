# Koncile OCR: Delete Template



```
DELETE https://connect.mindcloud.co/v1/universal/koncileOCR/latest/actions/delete-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Koncile OCR `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/koncileOCR/latest/actions/delete-template?connectionId=$CONNECTION_ID&template_id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "template_id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/koncileOCR/latest/actions/delete-template?${params}`, {
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
| `override` | boolean | no | Force deletion of documents inside this template when true. |
| `template_id` | number | yes | The template identifier to delete. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true,
      "template_id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean | Whether the delete request succeeded. |
| `template_id` | number | The deleted template identifier. |

## Native endpoint

Through the native Koncile OCR API, this operation is `DELETE /delete_template` (base URL `https://api.koncile.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-template.md) for the provider-specific parameters and requirements.

