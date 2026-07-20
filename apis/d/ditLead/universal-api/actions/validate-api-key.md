# DitLead: Validate API Key



```
GET https://connect.mindcloud.co/v1/universal/ditLead/latest/actions/validate-api-key
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DitLead `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ditLead/latest/actions/validate-api-key?connectionId=$CONNECTION_ID&keyType=platform" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "keyType": "platform"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ditLead/latest/actions/validate-api-key?${params}`, {
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
| `keyType` | string | yes | Key classification to validate. DitLead documents `platform` and `system`. One of: `0`, `1`. Default: `platform`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "apiKeyData": {
          "_id": "string",
          "name": "Ava Chen"
        },
        "keyType": "string",
        "projectData": {
          "id": "string",
          "name": "Ava Chen",
          "slug": "string"
        }
      },
      "isValid": true,
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.apiKeyData._id` | string | Internal API key identifier. |
| `data.apiKeyData.name` | string | API key display name. |
| `data.keyType` | string | Validated key classification. |
| `data.projectData.id` | string | Internal project identifier for the validated key. |
| `data.projectData.name` | string | Project name for the validated key. |
| `data.projectData.slug` | string | Workspace slug for the validated key. |
| `isValid` | boolean | Whether the API key is valid. |
| `success` | boolean | Whether the validation request succeeded. |

## Native endpoint

Through the native DitLead API, this operation is `POST /v1/apikey/validate` (base URL `https://api.ditlead.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/validate-api-key.md) for the provider-specific parameters and requirements.

