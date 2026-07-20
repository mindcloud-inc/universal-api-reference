# Kite Suite: Get forms by project ID



```
GET https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/get-forms-by-project-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kite Suite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/get-forms-by-project-id?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/get-forms-by-project-id?${params}`, {
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
| `id` | string | yes | project ID |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_id": "string",
      "avatar": {},
      "editable": true,
      "elements": [
        "string"
      ],
      "isTrashed": true,
      "label": "string",
      "owner": "string",
      "projectID": "string",
      "publicKey": "string",
      "status": "string",
      "statusCondition": {},
      "submissionCount": 1,
      "submissionType": "string",
      "title": "string",
      "workspace": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_id` | string | ID of the form |
| `avatar` | object | form avatar |
| `editable` | boolean |  |
| `elements` | array |  |
| `isTrashed` | boolean |  |
| `label` | string | labels of ids |
| `owner` | string |  |
| `projectID` | string | project ID of project |
| `publicKey` | string |  |
| `status` | string | status of form |
| `statusCondition` | object |  |
| `submissionCount` | number | number of submissions |
| `submissionType` | string | submission types |
| `title` | string | title |
| `workspace` | string | Id of workspace |

## Native endpoint

Through the native Kite Suite API, this operation is `GET /api/v1/form/project/:id` (base URL `https://api.kitesuite.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-forms-by-project-id.md) for the provider-specific parameters and requirements.

