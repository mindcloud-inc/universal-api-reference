# Nyckel: Get Function

Retrieves a function from Nyckel.

```
GET https://connect.mindcloud.co/v1/universal/nyckel/latest/actions/get-function
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nyckel `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nyckel/latest/actions/get-function?connectionId=$CONNECTION_ID&functionId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "functionId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nyckel/latest/actions/get-function?${params}`, {
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
| `functionId` | string | yes | Nyckel function identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "input": "string",
      "name": "Ava Chen",
      "output": "string",
      "projectId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `input` | string |  |
| `name` | string |  |
| `output` | string |  |
| `projectId` | string |  |

## Native endpoint

Through the native Nyckel API, this operation is `GET /functions/:functionId` (base URL `https://www.nyckel.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-function.md) for the provider-specific parameters and requirements.

