# Intelliprint: Retrieve Mailing List Recipient



```
GET https://connect.mindcloud.co/v1/universal/intelliprint/latest/actions/retrieve-mailing-list-recipient
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Intelliprint `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/intelliprint/latest/actions/retrieve-mailing-list-recipient?connectionId=$CONNECTION_ID&id=string&mailingList=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string",
  "mailingList": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/intelliprint/latest/actions/retrieve-mailing-list-recipient?${params}`, {
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
| `id` | string | yes | The Intelliprint mailing list recipient ID. |
| `mailingList` | string | yes | The Intelliprint mailing list ID. |

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

Through the native Intelliprint API, this operation is `GET /mailing_lists/:mailingList/recipients/:id` (base URL `https://api.intelliprint.net/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-mailing-list-recipient.md) for the provider-specific parameters and requirements.

