# Mendix: Update Project Categories

Updates project category assignments in Mendix.

```
PUT https://connect.mindcloud.co/v1/universal/mendix/latest/actions/update-project-categories
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mendix `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/mendix/latest/actions/update-project-categories" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectId": "d92064a5-b1fd-4be4-97db-53fc90201d1c"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mendix/latest/actions/update-project-categories', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectId": "d92064a5-b1fd-4be4-97db-53fc90201d1c"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `projectId` | string | yes | The unique identifier of a project. Example: `d92064a5-b1fd-4be4-97db-53fc90201d1c`. |
| `categories[]` | array<object> | no | Array of project category assignments. Each item identifies a company category and the value to assign or clear. Example: `[object Object]`. |

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
| `success` | boolean | Mendix documents no response body for this successful operation; this connector field represents request completion. |

## Native endpoint

Through the native Mendix API, this operation is `PATCH /projects/:projectId` (base URL `https://projects-api.home.mendix.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-project-categories.md) for the provider-specific parameters and requirements.

