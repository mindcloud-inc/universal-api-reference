# Damstra Forms: Get Project List

Retrieves a project list from Damstra Forms.

```
GET https://connect.mindcloud.co/v1/universal/damstraForms/latest/actions/get-project-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Damstra Forms `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/damstraForms/latest/actions/get-project-list?connectionId=$CONNECTION_ID&projectId=1&projectListTypeId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "1",
  "projectListTypeId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/damstraForms/latest/actions/get-project-list?${params}`, {
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
| `projectId` | string | yes | The unique id (numeric) or uuid (string) identifier of the project. Example: `1`. |
| `projectListTypeId` | string | yes | The unique id (numeric) or uuid (string) identifier of the project list type. Example: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "columnHeadings": [
        "string"
      ],
      "columnTypes": [
        "string"
      ],
      "createdAt": "2026-05-07T12:00:00.000Z",
      "itemTable": [
        [
          "string"
        ]
      ],
      "lockVersion": 1,
      "projectId": 1,
      "projectListTypeId": 1,
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `columnHeadings` | array<string> | From Damstra Forms API example response. |
| `columnTypes` | array<string> | From Damstra Forms API example response. |
| `createdAt` | date | From Damstra Forms API example response. |
| `itemTable` | array<array> | From Damstra Forms API example response. |
| `lockVersion` | number | From Damstra Forms API example response. |
| `projectId` | number | From Damstra Forms API example response. |
| `projectListTypeId` | number | From Damstra Forms API example response. |
| `updatedAt` | date | From Damstra Forms API example response. |

## Native endpoint

Through the native Damstra Forms API, this operation is `GET /projects/{project_id}/project_lists/{project_list_type_id}` (base URL `{{credentials.baseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-project-list.md) for the provider-specific parameters and requirements.

