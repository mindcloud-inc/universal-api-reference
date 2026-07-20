# Affinda: Get detail of an organization

Retrieves a specific organization from Affinda.

```
GET https://connect.mindcloud.co/v1/universal/affinda/latest/actions/get-organization
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Affinda `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/affinda/latest/actions/get-organization?connectionId=$CONNECTION_ID&identifier=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "identifier": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/affinda/latest/actions/get-organization?${params}`, {
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
| `identifier` | string | yes | Organization identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "avatar": "string",
      "identifier": "string",
      "isTrial": true,
      "name": "Ava Chen",
      "resthookSignatureKey": "string",
      "showCustomFieldCreation": true,
      "userRole": "string",
      "validationToolConfig": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `avatar` | string |  |
| `identifier` | string |  |
| `isTrial` | boolean |  |
| `name` | string |  |
| `resthookSignatureKey` | string |  |
| `showCustomFieldCreation` | boolean |  |
| `userRole` | string |  |
| `validationToolConfig` | object |  |

## Native endpoint

Through the native Affinda API, this operation is `GET /v3/organizations/:identifier` (base URL `https://api.us1.affinda.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-organization.md) for the provider-specific parameters and requirements.

