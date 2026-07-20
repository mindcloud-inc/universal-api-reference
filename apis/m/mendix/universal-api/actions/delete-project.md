# Mendix: Delete Project

Deletes an existing project from Mendix.

```
DELETE https://connect.mindcloud.co/v1/universal/mendix/latest/actions/delete-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mendix `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/mendix/latest/actions/delete-project?connectionId=$CONNECTION_ID&projectId=d92064a5-b1fd-4be4-97db-53fc90201d1c" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "d92064a5-b1fd-4be4-97db-53fc90201d1c"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mendix/latest/actions/delete-project?${params}`, {
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
| `projectId` | string | yes | The unique identifier of a project. Example: `d92064a5-b1fd-4be4-97db-53fc90201d1c`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean | Mendix documents an accepted no-body response; this connector field represents request completion. |

## Native endpoint

Through the native Mendix API, this operation is `DELETE /projects/:projectId` (base URL `https://projects-api.home.mendix.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-project.md) for the provider-specific parameters and requirements.

