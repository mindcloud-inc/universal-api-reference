# Damstra Forms: List Templates

Retrieves templates from Damstra Forms.

```
GET https://connect.mindcloud.co/v1/universal/damstraForms/latest/actions/list-templates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Damstra Forms `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/damstraForms/latest/actions/list-templates?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/damstraForms/latest/actions/list-templates?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `includeInactive` | boolean | no | Include inactive templates. Default: `false`. Example: `true`. |
| `type` | string | no | Return templates of the specified type(s). One of: `0`, `1`, `2`, `3`. Accepts multiple values in one string, delimited by `\|`. Default: `published`. Example: `draft\|archived\|published`. |
| `templateType` | string | no | Return only templates of a certain type. 1 = General Memo, 2 = Issue Memo, 3 = RFI Memo, 4 = Action, 5 = Form. One of: `0`, `1`, `2`, `3`, `4`. Example: `4`. |
| `updatedFrom` | string | no | Only return results updated after the specified value. It will try to make sense of whatever datetime format you provide, but the example shows the officially supported format. Example: `2016-12-31T13:50:00Z`. |
| `projectId` | string | no | The unique id (numeric) or uuid (string) of the project. Its purpose is to return results that belongs to a specific project. Example: `3d651680-2ace-43ac-b969-26b1da820b45`. |
| `showManaged` | boolean | no | Determines whether to include integrated templates in the response. Default: `false`. Example: `false`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "draftTemplate": {
        "href": "string",
        "id": 1
      },
      "href": "string",
      "id": 1,
      "name": "Ava Chen",
      "publishedVersion": 1,
      "templateType": 1,
      "type": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "version": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean | From Damstra Forms API example response. |
| `createdAt` | date | From Damstra Forms API example response. |
| `draftTemplate` | object | From Damstra Forms API example response. |
| `draftTemplate.href` | string | From Damstra Forms API example response. |
| `draftTemplate.id` | number | From Damstra Forms API example response. |
| `href` | string | From Damstra Forms API example response. |
| `id` | number | From Damstra Forms API example response. |
| `name` | string | From Damstra Forms API example response. |
| `publishedVersion` | number | From Damstra Forms API example response. |
| `templateType` | number | From Damstra Forms API example response. |
| `type` | string | From Damstra Forms API example response. |
| `updatedAt` | date | From Damstra Forms API example response. |
| `version` | string | From Damstra Forms API example response. |

## Native endpoint

Through the native Damstra Forms API, this operation is `GET /templates` (base URL `{{credentials.baseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-templates.md) for the provider-specific parameters and requirements.

