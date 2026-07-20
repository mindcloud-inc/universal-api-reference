# Vercel: Get Alias

Retrieves an alias record from Vercel.

```
GET https://connect.mindcloud.co/v1/universal/vercel/latest/actions/get-alias
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vercel `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vercel/latest/actions/get-alias?connectionId=$CONNECTION_ID&idOrAlias=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "idOrAlias": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vercel/latest/actions/get-alias?${params}`, {
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
| `idOrAlias` | string | yes | The alias string or alias ID to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "alias": "string",
      "createdAt": 1,
      "deploymentId": "string",
      "projectId": "string",
      "uid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `alias` | string |  |
| `createdAt` | number |  |
| `deploymentId` | string |  |
| `projectId` | string |  |
| `uid` | string |  |

## Native endpoint

Through the native Vercel API, this operation is `GET /v4/aliases/:idOrAlias` (base URL `https://api.vercel.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-alias.md) for the provider-specific parameters and requirements.

