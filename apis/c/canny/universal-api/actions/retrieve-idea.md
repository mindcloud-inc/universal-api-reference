# Canny: Retrieve Idea

Retrieves a single idea from Canny.

```
GET https://connect.mindcloud.co/v1/universal/canny/latest/actions/retrieve-idea
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Canny `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/canny/latest/actions/retrieve-idea?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/canny/latest/actions/retrieve-idea?${params}`, {
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
| `id` | string | no | The idea unique identifier. |
| `urlName` | string | no | The idea unique URL name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "author": {},
      "childCount": 1,
      "created": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "group": {},
      "id": "string",
      "owner": {},
      "parent": {},
      "source": {},
      "status": {},
      "title": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "urlName": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `author` | object |  |
| `childCount` | number |  |
| `created` | date |  |
| `description` | string |  |
| `group` | object |  |
| `id` | string |  |
| `owner` | object |  |
| `parent` | object |  |
| `source` | object |  |
| `status` | object |  |
| `title` | string |  |
| `updatedAt` | date |  |
| `urlName` | string |  |

## Native endpoint

Through the native Canny API, this operation is `POST /v1/ideas/retrieve` (base URL `https://canny.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-idea.md) for the provider-specific parameters and requirements.

