# Shuffll: Get Project Export Status

Retrieves project export status from Shuffll.

```
GET https://connect.mindcloud.co/v1/universal/shuffll/latest/actions/get-project-export-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Shuffll `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shuffll/latest/actions/get-project-export-status?connectionId=$CONNECTION_ID&projectId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shuffll/latest/actions/get-project-export-status?${params}`, {
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
| `projectId` | string | yes | Shuffll project id. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "isDone": true,
      "urls": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `isDone` | boolean | Whether export is complete. |
| `urls` | object | Export file URLs. |

## Native endpoint

Through the native Shuffll API, this operation is `GET /auth/project/:projectId/edit/status/export` (base URL `https://api.shuffll.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-project-export-status.md) for the provider-specific parameters and requirements.

