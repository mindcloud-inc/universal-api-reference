# Postman: Delete Environment

Deletes an existing environment from Postman.

```
DELETE https://connect.mindcloud.co/v1/universal/postman/latest/actions/delete-environment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Postman `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/postman/latest/actions/delete-environment?connectionId=$CONNECTION_ID&environmentId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "environmentId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/postman/latest/actions/delete-environment?${params}`, {
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
| `environmentId` | string | yes | The environment's ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "environment": {
        "id": "string",
        "uid": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `environment.id` | string |  |
| `environment.uid` | string |  |

## Native endpoint

Through the native Postman API, this operation is `DELETE /environments/:environmentId` (base URL `https://api.getpostman.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-environment.md) for the provider-specific parameters and requirements.

