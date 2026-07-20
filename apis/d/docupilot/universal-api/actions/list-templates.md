# Docupilot: List Templates

Retrieves templates from Docupilot.

```
GET https://connect.mindcloud.co/v1/universal/docupilot/latest/actions/list-templates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Docupilot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/docupilot/latest/actions/list-templates?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/docupilot/latest/actions/list-templates?${params}`, {
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
| `deliveryType` | list<string> | no | Filter templates by configured delivery type (supports multiple values) One of: `aws_s3`, `azure_blob_storage`, `box_drive`, `docu_sign`, `dropbox`, `email`, `eversign`, `google_drive`, `hellosign`, `one_drive`, `podio`, `sftp`, `sign_now`, `signable`, `signature`, `webhook`, `yousign`, `zoho_crm`. Accepts multiple values as an array. |
| `folder` | number | no |  |
| `ordering` | string | no | Which field to use when ordering the results. |
| `outputType` | list | no | One of: `docx`, `html`, `jpeg`, `pdf`, `png`, `pptx`, `xlsx`. |
| `page` | number | no | A page number within the paginated result set. |
| `search` | string | no | Search templates by title |
| `status` | list | no | Filter templates by status (all, active, test) One of: `active`, `test`. |
| `type` | list | no | One of: `docx`, `fillable_pdf`, `g_document`, `g_presentation`, `g_spreadsheet`, `html`, `pptx`, `xlsx`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Docupilot API returns.

## Native endpoint

Through the native Docupilot API, this operation is `GET /dashboard/api/v2/templates/` (base URL `https://api.docupilot.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-templates.md) for the provider-specific parameters and requirements.

