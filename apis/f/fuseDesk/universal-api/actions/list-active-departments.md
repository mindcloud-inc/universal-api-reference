# FuseDesk: List Active Departments

Retrieves active departments from your FuseDesk account.

```
GET https://connect.mindcloud.co/v1/universal/fuseDesk/latest/actions/list-active-departments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FuseDesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fuseDesk/latest/actions/list-active-departments?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fuseDesk/latest/actions/list-active-departments?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "allReps": true,
      "dateArchived": "2026-05-07T12:00:00.000Z",
      "dateCreated": "2026-05-07T12:00:00.000Z",
      "feedbackDelay": 1,
      "feedbackFrequency": 1,
      "feedbackSample": 1,
      "feedbackTemplateId": 1,
      "footerHtml": "string",
      "id": 1,
      "name": "Ava Chen",
      "newCaseNoteTemplateId": 1,
      "noteTemplateId": 1,
      "phone": "string",
      "replyTemplateId": 1,
      "repUserIds": [
        1
      ],
      "stale": 1,
      "staleWarning": 1,
      "templateCategory": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `allReps` | boolean |  |
| `dateArchived` | date |  |
| `dateCreated` | date |  |
| `feedbackDelay` | number |  |
| `feedbackFrequency` | number |  |
| `feedbackSample` | number |  |
| `feedbackTemplateId` | number |  |
| `footerHtml` | string |  |
| `id` | number |  |
| `name` | string |  |
| `newCaseNoteTemplateId` | number |  |
| `noteTemplateId` | number |  |
| `phone` | string |  |
| `replyTemplateId` | number |  |
| `repUserIds` | array<number> |  |
| `stale` | number |  |
| `staleWarning` | number |  |
| `templateCategory` | string |  |

## Native endpoint

Through the native FuseDesk API, this operation is `GET /api/v2/departments` (base URL `https://{{credentials.appName}}.fusedesk.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-active-departments.md) for the provider-specific parameters and requirements.

