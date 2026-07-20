# Xata: Get available extensions for image



```
GET https://connect.mindcloud.co/v1/universal/xata/latest/actions/list-extensions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Xata `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/xata/latest/actions/list-extensions?connectionId=$CONNECTION_ID&organizationID=string&image=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "organizationID": "string",
  "image": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/xata/latest/actions/list-extensions?${params}`, {
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
| `organizationID` | string | yes | Unique identifier of the organization to check instance type availability for |
| `image` | string | yes | Image for which we list extensions |
| `region` | string | no | Region to list extensions for image in |

## Response

```json
{
  "success": true,
  "data": [
    {
      "extensions": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `extensions` | array<object> | Array of available images with their properties |

## Native endpoint

Through the native Xata API, this operation is `GET /organizations/:organizationID/extensions` (base URL `https://api.xata.tech`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-extensions.md) for the provider-specific parameters and requirements.

