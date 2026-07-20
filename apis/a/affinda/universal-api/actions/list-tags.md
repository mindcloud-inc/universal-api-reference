# Affinda: Get list of all tags

Retrieves all accessible tags from Affinda.

```
GET https://connect.mindcloud.co/v1/universal/affinda/latest/actions/list-tags
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Affinda `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/affinda/latest/actions/list-tags?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/affinda/latest/actions/list-tags?${params}`, {
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
| `limit` | string | no | The numbers of results to return. |
| `name` | string | no | Filter by name. |
| `offset` | string | no | The number of documents to skip before starting to collect the result set. |
| `workspace` | string | no | Filter by workspace. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "documentCount": 1,
      "id": 1,
      "name": "Ava Chen",
      "workspace": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `documentCount` | number |  |
| `id` | number |  |
| `name` | string |  |
| `workspace` | string |  |

## Native endpoint

Through the native Affinda API, this operation is `GET /v3/tags` (base URL `https://api.us1.affinda.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-tags.md) for the provider-specific parameters and requirements.

