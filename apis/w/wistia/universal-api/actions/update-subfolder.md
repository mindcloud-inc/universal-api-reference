# Wistia: Update Subfolder

Updates an existing subfolder in Wistia.

```
PUT https://connect.mindcloud.co/v1/universal/wistia/latest/actions/update-subfolder
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wistia `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/wistia/latest/actions/update-subfolder" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectId": "string",
  "subfolderId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/wistia/latest/actions/update-subfolder', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectId": "string",
    "subfolderId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `projectId` | string | yes |  |
| `subfolderId` | string | yes |  |
| `name` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created": "2026-05-07T12:00:00.000Z",
      "cursor": "string",
      "description": "string",
      "hashedId": "string",
      "name": "Ava Chen",
      "position": 1,
      "updated": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | date | The date when the subfolder was created. |
| `cursor` | string | A cursor for stable pagination based on current `sort_by` order. You can pass this to `cursor[before]` or `cursor[after]` as a parameter to fetch the records before or after this record in the same sort order. This is only populated if records were fetched with `cursor[enabled]`, or `cursor[before]` or `cursor[after]`. |
| `description` | string | A description for the subfolder. |
| `hashedId` | string | A unique alphanumeric identifier for this subfolder. |
| `name` | string | The display name of the subfolder. |
| `position` | number | The position of this subfolder within its folder, used for ordering. |
| `updated` | date | The date when the subfolder was last modified. |

## Native endpoint

Through the native Wistia API, this operation is `PUT /v1/projects/:projectId/subfolders/:subfolderId` (base URL `https://api.wistia.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-subfolder.md) for the provider-specific parameters and requirements.

