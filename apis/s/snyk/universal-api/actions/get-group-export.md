# Snyk: Get Group Export

Retrieves an export from a Snyk group.

```
GET https://connect.mindcloud.co/v1/universal/snyk/latest/actions/get-group-export
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Snyk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/snyk/latest/actions/get-group-export?connectionId=$CONNECTION_ID&export_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "export_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/snyk/latest/actions/get-group-export?${params}`, {
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
| `export_id` | string | yes | Export ID for the request path. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "jsonapi": {},
      "links": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |
| `jsonapi` | object |  |
| `links` | object |  |

## Native endpoint

Through the native Snyk API, this operation is `GET /groups/:group_id/export/:export_id` (base URL `https://api.snyk.io/rest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-group-export.md) for the provider-specific parameters and requirements.

