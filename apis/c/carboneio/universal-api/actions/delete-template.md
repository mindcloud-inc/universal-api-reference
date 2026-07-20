# Carbone.io: Delete Template

Deletes a template from Carbone.io.

```
DELETE https://connect.mindcloud.co/v1/universal/carboneio/latest/actions/delete-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Carbone.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/carboneio/latest/actions/delete-template?connectionId=$CONNECTION_ID&templateIdOrVersionId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "templateIdOrVersionId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/carboneio/latest/actions/delete-template?${params}`, {
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
| `templateIdOrVersionId` | string | yes | Template ID (64-bit) or Version ID (SHA-256) to delete. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean | Whether the template deletion succeeded. |

## Native endpoint

Through the native Carbone.io API, this operation is `DELETE /template/[:templateId-or-versionId]` (base URL `https://api.carbone.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-template.md) for the provider-specific parameters and requirements.

