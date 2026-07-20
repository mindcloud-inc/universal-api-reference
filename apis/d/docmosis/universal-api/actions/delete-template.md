# Docmosis: Delete Template



```
DELETE https://connect.mindcloud.co/v1/universal/docmosis/latest/actions/delete-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Docmosis `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/docmosis/latest/actions/delete-template?connectionId=$CONNECTION_ID&templateName%5B%5D=%2Fmindcloud%2Fstage3%2Fdocmosis-stage3-template.docx" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "templateName[]": "/mindcloud/stage3/docmosis-stage3-template.docx"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/docmosis/latest/actions/delete-template?${params}`, {
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
| `templateName[]` | array<string> | yes | One or more template names to delete. Example: `/mindcloud/stage3/docmosis-stage3-template.docx`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "longMsg": "string",
      "shortMsg": "string",
      "succeeded": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `longMsg` | string |  |
| `shortMsg` | string |  |
| `succeeded` | boolean |  |

## Native endpoint

Through the native Docmosis API, this operation is `POST /deleteTemplate` (base URL `{{credentials.baseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-template.md) for the provider-specific parameters and requirements.

