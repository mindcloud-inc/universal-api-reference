# Poodll: Get Custom Action Details

Retrieves custom action field details from Poodll.

```
GET https://connect.mindcloud.co/v1/universal/poodll/latest/actions/get-custom-action-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Poodll `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/poodll/latest/actions/get-custom-action-details?connectionId=$CONNECTION_ID&customaction=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "customaction": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/poodll/latest/actions/get-custom-action-details?${params}`, {
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
| `customaction` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "field": "string",
      "fieldhelp": "string",
      "fieldname": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `field` | string |  |
| `fieldhelp` | string |  |
| `fieldname` | string |  |

## Native endpoint

Through the native Poodll API, this operation is `POST {{credentials.baseUrl}}/webservice/rest/server.php` (base URL `{{credentials.baseUrl}}/webservice/rest/server.php`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-custom-action-details.md) for the provider-specific parameters and requirements.

