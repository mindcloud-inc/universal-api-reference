# Stripo: Export Email to eSputnik

Exports an email from Stripo to eSputnik.

```
POST https://connect.mindcloud.co/v1/universal/stripo/latest/actions/export-email-to-esputnik
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stripo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/stripo/latest/actions/export-email-to-esputnik" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "accountEmail": "ava@example.com",
  "emailId": 1,
  "subject": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/stripo/latest/actions/export-email-to-esputnik', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "accountEmail": "ava@example.com",
    "emailId": 1,
    "subject": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `accountEmail` | string | yes | Email address linked to the eSputnik account. |
| `emailId` | number | yes | Email ID to export to eSputnik. |
| `subject` | string | yes | Subject line for the exported email. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean | Confirmation that the email export to eSputnik was accepted. |

## Native endpoint

Through the native Stripo API, this operation is `POST /export/esputnik` (base URL `https://my.stripo.email/emailgeneration/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/export-email-to-esputnik.md) for the provider-specific parameters and requirements.

