# Leverly: Salesforce Stop Call



```
DELETE https://connect.mindcloud.co/v1/universal/leverly/latest/actions/salesforce-stop-call
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Leverly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/leverly/latest/actions/salesforce-stop-call?connectionId=$CONNECTION_ID&id=string&phone=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string",
  "phone": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/leverly/latest/actions/salesforce-stop-call?${params}`, {
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
| `id` | string | yes | Salesforce lead ID sent in the outbound message. |
| `phone` | string | yes | Lead primary phone number. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "soapenv:Envelope": {
        "soapenv:Body": {
          "notifications": {
            "Ack": "string"
          }
        }
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `soapenv:Envelope.soapenv:Body.notifications.Ack` | string | SOAP acknowledgment returned by Leverly for the Salesforce stop-call notification. |

## Native endpoint

Through the native Leverly API, this operation is `POST /salesforce/unpark` (base URL `https://app.leverly.com/main`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/salesforce-stop-call.md) for the provider-specific parameters and requirements.

