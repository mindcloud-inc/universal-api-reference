# Hume: Get tool version



```
GET https://connect.mindcloud.co/v1/universal/hume/latest/actions/get-tool-version
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hume `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hume/latest/actions/get-tool-version?connectionId=$CONNECTION_ID&id=string&version=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string",
  "version": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hume/latest/actions/get-tool-version?${params}`, {
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
| `id` | string | yes | EVI tool identifier. |
| `version` | number | yes | Version number. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdOn": 1,
      "description": "string",
      "fallbackContent": "string",
      "id": "string",
      "modifiedOn": 1,
      "name": "Ava Chen",
      "parameters": "string",
      "toolType": "string",
      "version": 1,
      "versionDescription": "string",
      "versionType": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdOn` | number |  |
| `description` | string |  |
| `fallbackContent` | string |  |
| `id` | string |  |
| `modifiedOn` | number |  |
| `name` | string |  |
| `parameters` | string |  |
| `toolType` | string |  |
| `version` | number |  |
| `versionDescription` | string |  |
| `versionType` | string |  |

## Native endpoint

Through the native Hume API, this operation is `GET /v0/evi/tools/:id/version/:version` (base URL `https://api.hume.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-tool-version.md) for the provider-specific parameters and requirements.

