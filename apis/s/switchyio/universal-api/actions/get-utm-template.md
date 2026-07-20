# Switchy.io: Get UTM Template

Retrieves a UTM template from Switchy.io by ID.

```
GET https://connect.mindcloud.co/v1/universal/switchyio/latest/actions/get-utm-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Switchy.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/switchyio/latest/actions/get-utm-template?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/switchyio/latest/actions/get-utm-template?${params}`, {
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
| `id` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "campaign": "string",
      "content": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "medium": "string",
      "name": "Ava Chen",
      "source": "string",
      "term": "string",
      "workspaceId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `campaign` | string |  |
| `content` | string |  |
| `createdAt` | date |  |
| `id` | number |  |
| `medium` | string |  |
| `name` | string |  |
| `source` | string |  |
| `term` | string |  |
| `workspaceId` | number |  |

## Native endpoint

Through the native Switchy.io API, this operation is `POST /v1/graphql` (base URL `https://graphql.switchy.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-utm-template.md) for the provider-specific parameters and requirements.

