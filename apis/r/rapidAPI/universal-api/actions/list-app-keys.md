# RapidAPI: List App Keys

Retrieves app keys from RapidAPI.

```
GET https://connect.mindcloud.co/v1/universal/rapidAPI/latest/actions/list-app-keys
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RapidAPI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rapidAPI/latest/actions/list-app-keys?connectionId=$CONNECTION_ID&projectId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rapidAPI/latest/actions/list-app-keys?${params}`, {
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
| `projectId` | string | yes | RapidAPI app project ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "applicationEnvironmentName": "Ava Chen",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `applicationEnvironmentName` | string |  |
| `status` | string |  |

## Native endpoint

Through the native RapidAPI API, this operation is `GET /apps/{projectId}/keys` (base URL `{{credentials.baseUrlRest}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-app-keys.md) for the provider-specific parameters and requirements.

