# Cloze: Update Project

Updates a project in Cloze.

```
PUT https://connect.mindcloud.co/v1/universal/cloze/latest/actions/update-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cloze `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/cloze/latest/actions/update-project" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "MindCloud Stage 3 20260318-151600"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cloze/latest/actions/update-project', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "MindCloud Stage 3 20260318-151600"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `direct` | string | no | Direct identifier for the project to update. Example: `DznXZRdnRUEitVGpIW19lA`. |
| `name` | string | yes | Name of the project or deal. Example: `MindCloud Stage 3 20260318-151600`. |
| `summary` | string | no | Summary description of the project or deal. Example: `Updated during Stage 3 verification`. |
| `appLinks[]` | array<object> | no | App links used to identify and merge the project. |
| `appLinks[].source` | string | no | App domain name for the app link. |
| `appLinks[].uniqueid` | string | no | Unique identifier within the app link source. |

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

Through the native Cloze API, this operation is `POST /v1/projects/update` (base URL `https://api.cloze.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-project.md) for the provider-specific parameters and requirements.

