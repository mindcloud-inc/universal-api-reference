# Qase: Create a new shared parameter

Creates a new shared parameter in Qase.

```
POST https://connect.mindcloud.co/v1/universal/qase/latest/actions/create-shared-parameter
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Qase `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/qase/latest/actions/create-shared-parameter" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "title": "string",
  "type": "string",
  "isEnabledForAllProjects": true,
  "parameters": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/qase/latest/actions/create-shared-parameter', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "title": "string",
    "type": "string",
    "isEnabledForAllProjects": true,
    "parameters": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `title` | string | yes | Required request field title. |
| `type` | string | yes | Required request field type. |
| `isEnabledForAllProjects` | boolean | yes | Required request field is_enabled_for_all_projects. |
| `parameters` | string | yes | Required request field parameters. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |

## Native endpoint

Through the native Qase API, this operation is `POST /shared_parameter` (base URL `https://api.qase.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-shared-parameter.md) for the provider-specific parameters and requirements.

