# Routee: Retrieve Whatsapp template status

Retrieves WhatsApp template status from Routee.

```
GET https://connect.mindcloud.co/v1/universal/routee/latest/actions/retrieve-whatsapp-template-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Routee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/routee/latest/actions/retrieve-whatsapp-template-status?connectionId=$CONNECTION_ID&templateId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "templateId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/routee/latest/actions/retrieve-whatsapp-template-status?${params}`, {
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
| `templateId` | string | yes | Referenced template |

## Response

```json
{
  "success": true,
  "data": [
    {
      "localizations": [
        [
          {}
        ]
      ],
      "templateCategory": "string",
      "templateName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `localizations[]` | array<object> |  |
| `localizations[].components[]` | array<object> |  |
| `localizations[].components[].text` | string |  |
| `localizations[].components[].type` | string |  |
| `localizations[].language` | string |  |
| `localizations[].rejectionReason` | string |  |
| `localizations[].status` | string |  |
| `templateCategory` | string |  |
| `templateName` | string |  |

## Native endpoint

Through the native Routee API, this operation is `GET /accounts/templates/:templateId` (base URL `https://connect.routee.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-whatsapp-template-status.md) for the provider-specific parameters and requirements.

