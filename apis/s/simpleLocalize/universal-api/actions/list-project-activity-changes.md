# SimpleLocalize: List Project Activity Changes

Retrieves project activity changes from SimpleLocalize.

```
GET https://connect.mindcloud.co/v1/universal/simpleLocalize/latest/actions/list-project-activity-changes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SimpleLocalize `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/simpleLocalize/latest/actions/list-project-activity-changes?connectionId=$CONNECTION_ID&activityId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "activityId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/simpleLocalize/latest/actions/list-project-activity-changes?${params}`, {
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
| `activityId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "action": "string",
      "autoTranslatedBy": "string",
      "deprecatedAt": "2026-05-07T12:00:00.000Z",
      "key": "string",
      "language": "string",
      "namespace": "Ava Chen",
      "newKey": "string",
      "newNamespace": "Ava Chen",
      "occurred": "2026-05-07T12:00:00.000Z",
      "oldKey": "string",
      "oldNamespace": "Ava Chen",
      "overrideKey": "string",
      "reviewStatus": "string",
      "word": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `action` | string |  |
| `autoTranslatedBy` | string |  |
| `deprecatedAt` | date |  |
| `key` | string |  |
| `language` | string |  |
| `namespace` | string |  |
| `newKey` | string |  |
| `newNamespace` | string |  |
| `occurred` | date |  |
| `oldKey` | string |  |
| `oldNamespace` | string |  |
| `overrideKey` | string |  |
| `reviewStatus` | string |  |
| `word` | string |  |

## Native endpoint

Through the native SimpleLocalize API, this operation is `GET /api/v1/activity/{activityId}/changes` (base URL `https://api.simplelocalize.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-project-activity-changes.md) for the provider-specific parameters and requirements.

