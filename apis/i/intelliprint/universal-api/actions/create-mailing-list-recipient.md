# Intelliprint: Create Mailing List Recipient



```
POST https://connect.mindcloud.co/v1/universal/intelliprint/latest/actions/create-mailing-list-recipient
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Intelliprint `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/intelliprint/latest/actions/create-mailing-list-recipient" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "address.line": "string",
  "mailingList": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/intelliprint/latest/actions/create-mailing-list-recipient', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "address.line": "string",
    "mailingList": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `address.country` | string | no | ISO 3166-1 alpha-2 country code. |
| `address.line` | string | yes | The full mailing address line. |
| `address.name` | string | no | The recipient name printed on the mailing item. |
| `address.postcode` | string | no | The postal code for the address. |
| `mailingList` | string | yes | The Intelliprint mailing list ID. |
| `variables` | object | no | Dynamic template variables for the recipient. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "account": "string",
      "address": {},
      "address_validation_status": "string",
      "created": 1,
      "id": "string",
      "mailing_list": "string",
      "object": "string",
      "variables": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account` | string |  |
| `address` | object |  |
| `address_validation_status` | string |  |
| `created` | number |  |
| `id` | string |  |
| `mailing_list` | string |  |
| `object` | string |  |
| `variables` | object |  |

## Native endpoint

Through the native Intelliprint API, this operation is `POST /mailing_lists/:mailingList/recipients` (base URL `https://api.intelliprint.net/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-mailing-list-recipient.md) for the provider-specific parameters and requirements.

