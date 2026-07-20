# CircleCI: Delete URL Orb Allow List Entry



```
DELETE https://connect.mindcloud.co/v1/universal/circleCI/latest/actions/delete-url-orb-allow-list-entry
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CircleCI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/circleCI/latest/actions/delete-url-orb-allow-list-entry?connectionId=$CONNECTION_ID&allowListEntryId=string&orgSlugOrId=circleci%2FNheMuBArzQftQimV3Bqqky" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "allowListEntryId": "string",
  "orgSlugOrId": "circleci/NheMuBArzQftQimV3Bqqky"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/circleCI/latest/actions/delete-url-orb-allow-list-entry?${params}`, {
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
| `allowListEntryId` | string | yes | The URL orb allow-list entry UUID. |
| `orgSlugOrId` | string | yes | The CircleCI organization slug or ID. Default: `circleci/NheMuBArzQftQimV3Bqqky`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `message` | string |  |

## Native endpoint

Through the native CircleCI API, this operation is `DELETE /organization/:org_slug_or_id/url-orb-allow-list/:allow_list_entry_id` (base URL `https://circleci.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-url-orb-allow-list-entry.md) for the provider-specific parameters and requirements.

