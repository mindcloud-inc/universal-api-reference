# mittwald: Get App Version

Retrieves app version from mittwald API.

```
GET https://connect.mindcloud.co/v1/universal/mittwaldAPI/latest/actions/get-app-version
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a mittwald `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mittwaldAPI/latest/actions/get-app-version?connectionId=$CONNECTION_ID&appId=string&appVersionId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "appId": "string",
  "appVersionId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mittwaldAPI/latest/actions/get-app-version?${params}`, {
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
| `appVersionId` | string | yes | The unique identifier of the app version. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "appId": "string",
      "docRoot": "string",
      "docRootUserEditable": true,
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
| `docRoot` | string |  |
| `docRootUserEditable` | boolean |  |
| `externalVersion` | string |  |
| `id` | string |  |
| `internalVersion` | string |  |
| `recommended` | boolean |  |

## Native endpoint

Through the native mittwald API, this operation is `GET /v2/apps/:appId/versions/:appVersionId` (base URL `https://api.mittwald.de`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-app-version.md) for the provider-specific parameters and requirements.

