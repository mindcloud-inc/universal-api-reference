# Cloze: Create Project

Creates a project in Cloze.

```
POST https://connect.mindcloud.co/v1/universal/cloze/latest/actions/create-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cloze `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/cloze/latest/actions/create-project" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cloze/latest/actions/create-project', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | no | Name of the project or deal. |
| `summary` | string | no | Summary description of the project or deal. |
| `stage` | string | no | Stage of the project. One of: `0`, `1`, `2`, `3`. |
| `segment` | string | no | Segment of the project. |
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

Through the native Cloze API, this operation is `POST /v1/projects/create` (base URL `https://api.cloze.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-project.md) for the provider-specific parameters and requirements.

