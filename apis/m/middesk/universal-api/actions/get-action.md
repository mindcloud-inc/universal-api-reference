# Middesk: Retrieve an action

Retrieves an action from your Middesk account.

```
GET https://connect.mindcloud.co/v1/universal/middesk/latest/actions/get-action
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Middesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/middesk/latest/actions/get-action?connectionId=$CONNECTION_ID&id=string&objectId=string&objectType=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string",
  "objectId": "string",
  "objectType": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/middesk/latest/actions/get-action?${params}`, {
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
| `id` | string | yes | ID of the action to retrieve. |
| `objectId` | string | yes | ID of the object associated with the action. |
| `objectType` | string | yes | Type of object associated with the action. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "actors": [
        {}
      ],
      "createdAt": "string",
      "effects": [
        {}
      ],
      "id": "string",
      "metadata": {},
      "note": "string",
      "objectId": "string",
      "objectType": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `actors` | array<object> |  |
| `createdAt` | string |  |
| `effects` | array<object> |  |
| `id` | string |  |
| `metadata` | object |  |
| `note` | string |  |
| `objectId` | string |  |
| `objectType` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Middesk API, this operation is `GET /actions/:id` (base URL `https://api.middesk.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-action.md) for the provider-specific parameters and requirements.

