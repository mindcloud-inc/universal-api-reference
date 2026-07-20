# E2B: List Templates

Retrieves a list of templates from E2B.

```
GET https://connect.mindcloud.co/v1/universal/e2B/latest/actions/list-templates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a E2B `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/e2B/latest/actions/list-templates?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/e2B/latest/actions/list-templates?${params}`, {
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
| `teamId` | string | no | Identifier of the team. |

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
| `names` | array<string> | Template names. |
| `public` | boolean | Whether the template is public or team-only. |
| `templateID` | string | Identifier of the template. |
| `updatedAt` | date | Last update time. |

## Native endpoint

Through the native E2B API, this operation is `GET /templates` (base URL `https://api.e2b.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-templates.md) for the provider-specific parameters and requirements.

