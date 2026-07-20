# Lokalise: Delete Contributor

Deletes an existing contributor from Lokalise.

```
DELETE https://connect.mindcloud.co/v1/universal/lokalise/latest/actions/delete-contributor
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lokalise `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/lokalise/latest/actions/delete-contributor?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lokalise/latest/actions/delete-contributor?${params}`, {
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
| `contributor_id` | string | no | Lokalise contributor identifier. |
| `project_id` | string | no | Lokalise project identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contributor_deleted": true,
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
| `contributor_deleted` | boolean |  |
| `project_id` | string |  |
| `project_uuid` | string |  |

## Native endpoint

Through the native Lokalise API, this operation is `DELETE /projects/:project_id/contributors/:contributor_id` (base URL `https://api.lokalise.com/api2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-contributor.md) for the provider-specific parameters and requirements.

