# Refiner: List Forms

Retrieves forms from your Refiner account.

```
GET https://connect.mindcloud.co/v1/universal/refiner/latest/actions/list-forms
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Refiner `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/refiner/latest/actions/list-forms?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/refiner/latest/actions/list-forms?${params}`, {
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
| `list` | string | no | Choose which forms to return: all, published, drafts, archived, or all_with_archived. |
| `includeConfig` | boolean | no | Include the survey configuration and elements. |
| `includeInfo` | boolean | no | Include additional form metadata such as counts and dates. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archivedAt": "2026-05-07T12:00:00.000Z",
      "channels": [
        "string"
      ],
      "createdAt": "2026-05-07T12:00:00.000Z",
      "firstFormViewAt": "2026-05-07T12:00:00.000Z",
      "folder": {},
      "lastFormViewAt": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "pageUrl": "https://example.com",
      "publishedAt": "2026-05-07T12:00:00.000Z",
      "responsesCount": 1,
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "uuid": "string",
      "viewsCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archivedAt` | date |  |
| `channels` | array<string> |  |
| `createdAt` | date |  |
| `firstFormViewAt` | date |  |
| `folder` | object |  |
| `lastFormViewAt` | date |  |
| `name` | string |  |
| `pageUrl` | string |  |
| `publishedAt` | date |  |
| `responsesCount` | number |  |
| `updatedAt` | date |  |
| `uuid` | string |  |
| `viewsCount` | number |  |

## Native endpoint

Through the native Refiner API, this operation is `GET /forms` (base URL `https://api.refiner.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-forms.md) for the provider-specific parameters and requirements.

