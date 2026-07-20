# Productboard: Get Release

Retrieves a release from your Productboard workspace.

```
GET https://connect.mindcloud.co/v1/universal/productboard/latest/actions/get-release
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Productboard `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/productboard/latest/actions/get-release?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/productboard/latest/actions/get-release?${params}`, {
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
| `id` | string | yes | Release ID from Productboard. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archived": true,
      "description": "string",
      "id": "string",
      "links": {},
      "name": "Ava Chen",
      "releaseGroup": {},
      "state": "string",
      "timeframe": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archived` | boolean | Whether the release is archived. |
| `description` | string | Rich-text release description. |
| `id` | string | Productboard release identifier. |
| `links` | object | API links for the release. |
| `name` | string | Release name. |
| `releaseGroup` | object | Release group reference. |
| `state` | string | Release state. |
| `timeframe` | object | Release timeframe metadata. |

## Native endpoint

Through the native Productboard API, this operation is `GET /releases/:id` (base URL `https://api.productboard.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-release.md) for the provider-specific parameters and requirements.

