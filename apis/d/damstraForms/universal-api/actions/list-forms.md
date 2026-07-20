# Damstra Forms: List Forms

Retrieves forms from Damstra Forms.

```
GET https://connect.mindcloud.co/v1/universal/damstraForms/latest/actions/list-forms
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Damstra Forms `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/damstraForms/latest/actions/list-forms?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/damstraForms/latest/actions/list-forms?${params}`, {
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
| `draftTemplateId` | number | no | Only return forms associate with the specified draft template. Note that there can be many published versions of a given template, so you need to use draft_template_id if you to get all forms for that template regardless of version. Example: `101`. |
| `fullyApproved` | boolean | no | Only return forms where all approval sections have been approved (or where there are no approval sections) Default: `false`. Example: `true`. |
| `projectId` | number | no | Only return forms associate with the specified project. Example: `101`. |
| `raisedFrom` | string | no | Return forms where date raised is greater than or equal to the specified date. Example: `2016-12-01`. |
| `raisedTo` | string | no | Return forms where date raised is less than or equal to the specified date. Example: `2017-01-31`. |
| `status` | string | no | Statuses to include in returned results. You can combine statuses by separating them with "\|" (e.g. draft\|open, open\|closed, etc.) One of: `0`, `1`, `2`, `3`. Accepts multiple values in one string, delimited by `\|`. Default: `draft\|open\|closed`. Example: `closed`. |
| `templateId` | number | no | Only return forms associate with the specified published version of a template. See also draft_template_id. Example: `101`. |
| `updatedFrom` | string | no | Only return results updated after the specified value. It will try to make sense of whatever datetime format you provide, but the example shows the officially supported format. Example: `2016-12-31T13:50:00Z`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "clientCreatedAt": "2026-05-07T12:00:00.000Z",
      "clientUpdatedAt": "2026-05-07T12:00:00.000Z",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "createdByUserId": 1,
      "dateRaised": "2026-05-07T12:00:00.000Z",
      "draftTemplateId": 1,
      "href": "string",
      "id": 1,
      "ownedByUserId": 1,
      "sequenceNumber": 1,
      "shortDescription": "string",
      "status": 1,
      "templateId": 1,
      "templateName": "Ava Chen",
      "type": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "wbsItem": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `clientCreatedAt` | date | From Damstra Forms API example response. |
| `clientUpdatedAt` | date | From Damstra Forms API example response. |
| `createdAt` | date | From Damstra Forms API example response. |
| `createdByUserId` | number | From Damstra Forms API example response. |
| `dateRaised` | date | From Damstra Forms API example response. |
| `draftTemplateId` | number | From Damstra Forms API example response. |
| `href` | string | From Damstra Forms API example response. |
| `id` | number | From Damstra Forms API example response. |
| `ownedByUserId` | number | From Damstra Forms API example response. |
| `sequenceNumber` | number | From Damstra Forms API example response. |
| `shortDescription` | string | From Damstra Forms API example response. |
| `status` | number | From Damstra Forms API example response. |
| `templateId` | number | From Damstra Forms API example response. |
| `templateName` | string | From Damstra Forms API example response. |
| `type` | string | From Damstra Forms API example response. |
| `updatedAt` | date | From Damstra Forms API example response. |
| `wbsItem` | number | From Damstra Forms API example response. |

## Native endpoint

Through the native Damstra Forms API, this operation is `GET /forms` (base URL `{{credentials.baseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-forms.md) for the provider-specific parameters and requirements.

