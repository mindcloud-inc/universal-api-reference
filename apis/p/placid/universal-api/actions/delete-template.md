# Placid: Delete Template

Deletes an existing template from Placid.

```
DELETE https://connect.mindcloud.co/v1/universal/placid/latest/actions/delete-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Placid `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/placid/latest/actions/delete-template?connectionId=$CONNECTION_ID&templateUuid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "templateUuid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/placid/latest/actions/delete-template?${params}`, {
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
| `templateUuid` | string | yes | UUID of the template to delete. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "deleted": true,
      "deletedId": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `deleted` | boolean |  |
| `deletedId` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Placid API, this operation is `DELETE /api/rest/templates/:templateUuid` (base URL `https://api.placid.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-template.md) for the provider-specific parameters and requirements.

