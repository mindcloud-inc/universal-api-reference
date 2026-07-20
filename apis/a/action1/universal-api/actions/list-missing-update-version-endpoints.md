# Action1: List Missing Update Version Endpoints

Retrieves endpoints missing a specific update version in Action1.

```
GET https://connect.mindcloud.co/v1/universal/action1/latest/actions/list-missing-update-version-endpoints
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Action1 `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/action1/latest/actions/list-missing-update-version-endpoints?connectionId=$CONNECTION_ID&limit=25&offset=0&orgId=string&packageId=package-123&versionId=version-1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "orgId": "string",
  "packageId": "package-123",
  "versionId": "version-1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/action1/latest/actions/list-missing-update-version-endpoints?${params}`, {
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
| `orgId` | string | yes | Action1 organization ID. |
| `packageId` | string | yes | Missing update package ID. Example: `package-123`. |
| `versionId` | string | yes | Update version ID. Example: `version-1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "installed_version": "string",
      "name": "Ava Chen",
      "self": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `installed_version` | string |  |
| `name` | string |  |
| `self` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Action1 API, this operation is `GET /updates/:orgId/:packageId/versions/:versionId/endpoints` (base URL `https://app.action1.com/api/3.0`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-missing-update-version-endpoints.md) for the provider-specific parameters and requirements.

