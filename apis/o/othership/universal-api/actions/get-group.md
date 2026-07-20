# Othership: Get Group

Retrieves a specific group from Othership.

```
GET https://connect.mindcloud.co/v1/universal/othership/latest/actions/get-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Othership `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/othership/latest/actions/get-group?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/othership/latest/actions/get-group?${params}`, {
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
| `id` | string | yes | The SCIM group identifier. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `attributes` | string | no | Comma-separated SCIM attributes to include in the response. |
| `excludedAttributes` | string | no | Comma-separated SCIM attributes to omit from the response. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "displayName": "Ava Chen",
      "id": "string",
      "meta": {
        "resourceType": "string"
      },
      "schemas": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `displayName` | string |  |
| `id` | string |  |
| `meta.resourceType` | string |  |
| `schemas[]` | string |  |

## Native endpoint

Through the native Othership API, this operation is `GET /Groups/:id` (base URL `https://hwms-api.othership.com/api/v1/azure/scim`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-group.md) for the provider-specific parameters and requirements.

