# IndyForms: List Forms



```
GET https://connect.mindcloud.co/v1/universal/indyForms/latest/actions/list-forms
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a IndyForms `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/indyForms/latest/actions/list-forms?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/indyForms/latest/actions/list-forms?${params}`, {
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
| `partialName` | string | no |  |
| `status` | number | no |  |
| `access` | number | no |  |
| `createdAt.from` | date | no |  |
| `createdAt.to` | date | no |  |
| `keywords` | string | no |  |
| `rangeStart` | number | no |  |
| `rangeEnd` | number | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "completedRecordCount": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "folder": "string",
      "id": "string",
      "isLive": true,
      "name": "Ava Chen",
      "recordCount": 1,
      "tags": [
        "string"
      ],
      "version": 1,
      "versionId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `completedRecordCount` | number |  |
| `createdAt` | date |  |
| `folder` | string |  |
| `id` | string |  |
| `isLive` | boolean |  |
| `name` | string |  |
| `recordCount` | number |  |
| `tags` | array<string> |  |
| `version` | number |  |
| `versionId` | string |  |

## Native endpoint

Through the native IndyForms API, this operation is `GET /api/public/v2/forms` (base URL `https://api.indyforms.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-forms.md) for the provider-specific parameters and requirements.

