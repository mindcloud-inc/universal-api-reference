# Usedesk: Get Client

Retrieves a client by ID from Usedesk.

```
GET https://connect.mindcloud.co/v1/universal/usedesk/latest/actions/get-client
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Usedesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/usedesk/latest/actions/get-client?connectionId=$CONNECTION_ID&clientId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "clientId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/usedesk/latest/actions/get-client?${params}`, {
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
| `clientId` | number | yes | Client ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "addresses": [
        {}
      ],
      "client": {},
      "client_company": {},
      "emails": [
        {}
      ],
      "messengers": [
        {}
      ],
      "phones": [
        {}
      ],
      "sites": [
        {}
      ],
      "social_networks": [
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
| `addresses` | array<object> |  |
| `client` | object |  |
| `client_company` | object |  |
| `emails` | array<object> |  |
| `messengers` | array<object> |  |
| `phones` | array<object> |  |
| `sites` | array<object> |  |
| `social_networks` | array<object> |  |

## Native endpoint

Through the native Usedesk API, this operation is `POST /client` (base URL `https://secure.usedesk.com/uapi`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-client.md) for the provider-specific parameters and requirements.

