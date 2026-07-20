# Localazy: Delete Screenshot

Deletes an existing screenshot from a Localazy project.

```
DELETE https://connect.mindcloud.co/v1/universal/localazy/latest/actions/delete-screenshot
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Localazy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/localazy/latest/actions/delete-screenshot?connectionId=$CONNECTION_ID&projectId=string&screenshotId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "string",
  "screenshotId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/localazy/latest/actions/delete-screenshot?${params}`, {
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
| `projectId` | string | yes | Localazy project identifier or slug. |
| `screenshotId` | string | yes | Identifier of the screenshot to delete. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "result": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `result` | boolean | Whether the screenshot was deleted successfully. |

## Native endpoint

Through the native Localazy API, this operation is `DELETE /projects/:projectId/screenshots/:screenshotId` (base URL `https://api.localazy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-screenshot.md) for the provider-specific parameters and requirements.

