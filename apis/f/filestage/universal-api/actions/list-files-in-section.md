# Filestage: List Files in Section

Retrieves files from a Filestage section.

```
GET https://connect.mindcloud.co/v1/universal/filestage/latest/actions/list-files-in-section
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Filestage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/filestage/latest/actions/list-files-in-section?connectionId=$CONNECTION_ID&sectionId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "sectionId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/filestage/latest/actions/list-files-in-section?${params}`, {
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
| `sectionId` | string | yes | Section Id |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created": "2026-05-07T12:00:00.000Z",
      "externalId": "string",
      "id": "string",
      "name": "Ava Chen",
      "projectId": "string",
      "reviewLink": "https://example.com",
      "sectionId": "string",
      "versions": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | date |  |
| `externalId` | string |  |
| `id` | string |  |
| `name` | string |  |
| `projectId` | string |  |
| `reviewLink` | string |  |
| `sectionId` | string |  |
| `versions` | array<object> |  |

## Native endpoint

Through the native Filestage API, this operation is `GET /sections/{sectionId}/files` (base URL `https://api.filestage.io/ext/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-files-in-section.md) for the provider-specific parameters and requirements.

