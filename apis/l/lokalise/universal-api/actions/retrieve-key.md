# Lokalise: Retrieve Key

Retrieves a key from a Lokalise project.

```
GET https://connect.mindcloud.co/v1/universal/lokalise/latest/actions/retrieve-key
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lokalise `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lokalise/latest/actions/retrieve-key?connectionId=$CONNECTION_ID&project_id=string&key_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "project_id": "string",
  "key_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lokalise/latest/actions/retrieve-key?${params}`, {
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
| `project_id` | string | yes | Lokalise project identifier. |
| `key_id` | string | yes | Lokalise key identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "key": {},
      "project_id": "string",
      "project_uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `key` | object |  |
| `project_id` | string |  |
| `project_uuid` | string |  |

## Native endpoint

Through the native Lokalise API, this operation is `GET /projects/:project_id/keys/:key_id` (base URL `https://api.lokalise.com/api2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-key.md) for the provider-specific parameters and requirements.

