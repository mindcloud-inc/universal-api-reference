# Channels: List Contact Alternative MSISDNs

Retrieves alternative contact phone numbers from Channels.

```
GET https://connect.mindcloud.co/v1/universal/channels/latest/actions/list-contact-alternative-msisd-ns
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Channels `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/channels/latest/actions/list-contact-alternative-msisd-ns?connectionId=$CONNECTION_ID&contactId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "contactId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/channels/latest/actions/list-contact-alternative-msisd-ns?${params}`, {
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
| `contactId` | number | yes | Contact ID whose alternative MSISDNs should be returned. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "": [
        {
          "id": 1,
          "msisdn": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `[].id` | number |  |
| `[].msisdn` | string |  |

## Native endpoint

Through the native Channels API, this operation is `GET /api/v1/contacts/{contactId}/alternative-msisdns` (base URL `https://api.channels.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-contact-alternative-msisd-ns.md) for the provider-specific parameters and requirements.

