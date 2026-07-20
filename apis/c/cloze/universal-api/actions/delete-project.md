# Cloze: Delete Project

Deletes a project from Cloze.

```
DELETE https://connect.mindcloud.co/v1/universal/cloze/latest/actions/delete-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cloze `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/cloze/latest/actions/delete-project?connectionId=$CONNECTION_ID&uniqueid=mindcloudstage3.com%3Aflat-20260318-151600" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "uniqueid": "mindcloudstage3.com:flat-20260318-151600"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cloze/latest/actions/delete-project?${params}`, {
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
| `uniqueid` | string | yes | Project unique direct identifier or custom identifier. Example: `mindcloudstage3.com:flat-20260318-151600`. |
| `team` | boolean | no | Delete the team relation instead of the local relation. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "errorcode": 1,
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `errorcode` | number | Error code. 0 means success. |
| `message` | string | Human-readable error description when the request fails. |

## Native endpoint

Through the native Cloze API, this operation is `DELETE /v1/projects/delete` (base URL `https://api.cloze.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-project.md) for the provider-specific parameters and requirements.

