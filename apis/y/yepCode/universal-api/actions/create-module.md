# YepCode: Create module

Creates a new module in YepCode.

```
POST https://connect.mindcloud.co/v1/universal/yepCode/latest/actions/create-module
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a YepCode `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/yepCode/latest/actions/create-module" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "programmingLanguage": "string",
  "sourceCode": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/yepCode/latest/actions/create-module', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "programmingLanguage": "string",
    "sourceCode": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes |  |
| `programmingLanguage` | string | yes |  |
| `sourceCode` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "createdBy": "string",
      "id": "string",
      "name": "Ava Chen",
      "programmingLanguage": "string",
      "sourceCode": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "updatedBy": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `createdBy` | string |  |
| `id` | string |  |
| `name` | string |  |
| `programmingLanguage` | string |  |
| `sourceCode` | string |  |
| `updatedAt` | date |  |
| `updatedBy` | string |  |

## Native endpoint

Through the native YepCode API, this operation is `POST /modules` (base URL `https://cloud.yepcode.io/api/{{credentials.team}}/rest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-module.md) for the provider-specific parameters and requirements.

