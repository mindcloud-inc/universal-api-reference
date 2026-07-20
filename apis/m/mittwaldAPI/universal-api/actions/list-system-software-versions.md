# mittwald: List System Software Versions

Retrieves system software versions from mittwald API.

```
GET https://connect.mindcloud.co/v1/universal/mittwaldAPI/latest/actions/list-system-software-versions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a mittwald `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mittwaldAPI/latest/actions/list-system-software-versions?connectionId=$CONNECTION_ID&systemSoftwareId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "systemSoftwareId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mittwaldAPI/latest/actions/list-system-software-versions?${params}`, {
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
| `systemSoftwareId` | string | yes | The system software ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "expiryDate": "2026-05-07T12:00:00.000Z",
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
| `expiryDate` | date |  |
| `externalVersion` | string |  |
| `id` | string |  |
| `internalVersion` | string |  |
| `recommended` | boolean |  |

## Native endpoint

Through the native mittwald API, this operation is `GET /v2/system-softwares/:systemSoftwareId/versions` (base URL `https://api.mittwald.de`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-system-software-versions.md) for the provider-specific parameters and requirements.

