# Formstack: Delete Form

Deletes a form from Formstack by marking it as deleted.

```
DELETE https://connect.mindcloud.co/v1/universal/formstack/latest/actions/delete-form
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Formstack `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/formstack/latest/actions/delete-form?connectionId=$CONNECTION_ID&formId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "formId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/formstack/latest/actions/delete-form?${params}`, {
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
| `formId` | list<number> | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "created": "2026-05-07T12:00:00.000Z",
      "dataUrl": "https://example.com",
      "db": true,
      "deleted": true,
      "editUrl": "https://example.com",
      "encrypted": true,
      "folder": 1,
      "id": 1,
      "inactive": true,
      "isWorkflowForm": true,
      "isWorkflowPublished": true,
      "language": "string",
      "name": "Ava Chen",
      "numberOfColumns": "string",
      "progressMeter": "string",
      "shouldDisplayOneQuestionAtATime": true,
      "submissions": "string",
      "submissionsCount": 1,
      "submissionsUnread": "string",
      "submitButtonTitle": "string",
      "summaryUrl": "https://example.com",
      "thumbnailUrl": "https://example.com",
      "timezone": "string",
      "unreadSubmissionsCount": 1,
      "updated": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com",
      "version": "string",
      "viewKey": "string",
      "views": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean | Whether the form is active. |
| `created` | date | Date of form creation. |
| `dataUrl` | string | URL to form data. |
| `db` | boolean | Whether submissions are saved to the database. |
| `deleted` | boolean | Whether the form is deleted. |
| `editUrl` | string | URL to edit the form. |
| `encrypted` | boolean | Whether the form is encrypted. |
| `folder` | number | ID of the folder where the form is located. |
| `id` | number | The ID of the form. |
| `inactive` | boolean | Whether the form is inactive. |
| `isWorkflowForm` | boolean | Whether the form is a workflow form. |
| `isWorkflowPublished` | boolean | Whether the workflow form is published. |
| `language` | string | Form language. |
| `name` | string | Name of the form. |
| `numberOfColumns` | string | Number of visible columns in the form. |
| `progressMeter` | string | Whether progress meter is enabled. |
| `shouldDisplayOneQuestionAtATime` | boolean | Whether the form should display one question at a time. |
| `submissions` | string | Number of submissions. |
| `submissionsCount` | number | Count of form submissions. |
| `submissionsUnread` | string | Number of unread submissions. |
| `submitButtonTitle` | string | Title of the submit button. |
| `summaryUrl` | string | URL to form summary. |
| `thumbnailUrl` | string | URL to form thumbnail. |
| `timezone` | string | Form timezone. |
| `unreadSubmissionsCount` | number | Count of unread form submissions. |
| `updated` | date | Date of last update. |
| `url` | string | URL of the live form. |
| `version` | string | Form version. |
| `viewKey` | string | View key of the form. |
| `views` | string | Number of form views. |

## Native endpoint

Through the native Formstack API, this operation is `DELETE /forms/:formId` (base URL `https://www.formstack.com/api/v2025`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-form.md) for the provider-specific parameters and requirements.

