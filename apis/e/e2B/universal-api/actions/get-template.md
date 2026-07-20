# E2B: Get Template

Retrieves a template from E2B.

```
GET https://connect.mindcloud.co/v1/universal/e2B/latest/actions/get-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a E2B `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/e2B/latest/actions/get-template?connectionId=$CONNECTION_ID&templateId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "templateId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/e2B/latest/actions/get-template?${params}`, {
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
      "builds": [
        {}
      ],
      "createdAt": "2026-05-07T12:00:00.000Z",
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
| `builds` | array<object> | Builds for the template. |
| `createdAt` | date | Creation time. |
| `lastSpawnedAt` | date | Last time a sandbox was spawned from the template. |
| `names` | array<string> | Template names. |
| `public` | boolean | Whether the template is public. |
| `templateID` | string | Identifier of the template. |
| `updatedAt` | date | Last update time. |

## Native endpoint

Through the native E2B API, this operation is `GET /templates/{templateID}` (base URL `https://api.e2b.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-template.md) for the provider-specific parameters and requirements.

