# E2B: Rebuild Template

Rebuilds a template in E2B.

```
PUT https://connect.mindcloud.co/v1/universal/e2B/latest/actions/rebuild-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a E2B `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/e2B/latest/actions/rebuild-template" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "templateId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/e2B/latest/actions/rebuild-template', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "templateId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `templateId` | string | yes | Identifier of the template. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "aliases": [
        "string"
      ],
      "buildID": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "createdBy": {},
      "lastSpawnedAt": "2026-05-07T12:00:00.000Z",
      "names": [
        "Ava Chen"
      ],
      "public": true,
      "templateID": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `aliases` | array<string> | Template aliases. |
| `buildID` | string | Identifier of the last successful build for the template. |
| `createdAt` | date | Creation time. |
| `createdBy` | object | Creator details. |
| `lastSpawnedAt` | date | Last time a sandbox was spawned from the template. |
| `names` | array<string> | Template names. |
| `public` | boolean | Whether the template is public. |
| `templateID` | string | Identifier of the template. |
| `updatedAt` | date | Last update time. |

## Native endpoint

Through the native E2B API, this operation is `POST /templates/{templateID}` (base URL `https://api.e2b.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/rebuild-template.md) for the provider-specific parameters and requirements.

