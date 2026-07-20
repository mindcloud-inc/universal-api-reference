# Documentum: Get Encrypted DM Ticket



```
GET https://connect.mindcloud.co/v1/universal/documentum/latest/actions/get-encrypted-dm-ticket
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Documentum `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/documentum/latest/actions/get-encrypted-dm-ticket?connectionId=$CONNECTION_ID&repositoryName=d2repo" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "repositoryName": "d2repo"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/documentum/latest/actions/get-encrypted-dm-ticket?${params}`, {
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
| `repositoryName` | string | yes | Documentum repository name. Example: `d2repo`. |
| `secure` | boolean | no | Set to true to request an encrypted DM ticket. Default: `true`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "secure": true,
      "ticket": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `secure` | boolean | Whether the ticket request used secure mode. |
| `ticket` | string | Encrypted DM ticket. |

## Native endpoint

Through the native Documentum API, this operation is `GET /repositories/{repositoryName}/dm-ticket` (base URL `{{credentials.documentumRestBaseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-encrypted-dm-ticket.md) for the provider-specific parameters and requirements.

