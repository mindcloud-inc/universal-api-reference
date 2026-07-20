# mittwald: List App Version Update Candidates

Retrieves app version update candidates from mittwald API.

```
GET https://connect.mindcloud.co/v1/universal/mittwaldAPI/latest/actions/list-app-version-update-candidates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a mittwald `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mittwaldAPI/latest/actions/list-app-version-update-candidates?connectionId=$CONNECTION_ID&appId=string&baseAppVersionId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "appId": "string",
  "baseAppVersionId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mittwaldAPI/latest/actions/list-app-version-update-candidates?${params}`, {
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
| `appId` | string | yes | The unique identifier of the app. |
| `baseAppVersionId` | string | yes | The unique identifier of the base app version. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "appId": "string",
      "externalVersion": "string",
      "id": "string",
      "internalVersion": "string",
      "recommended": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `appId` | string |  |
| `externalVersion` | string |  |
| `id` | string |  |
| `internalVersion` | string |  |
| `recommended` | boolean |  |

## Native endpoint

Through the native mittwald API, this operation is `GET /v2/apps/:appId/versions/:baseAppVersionId/update-candidates` (base URL `https://api.mittwald.de`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-app-version-update-candidates.md) for the provider-specific parameters and requirements.

