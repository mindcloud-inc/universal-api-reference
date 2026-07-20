# Simplicate: Get Quote Template



```
GET https://connect.mindcloud.co/v1/universal/simplicate/latest/actions/get-quote-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Simplicate `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/simplicate/latest/actions/get-quote-template?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/simplicate/latest/actions/get-quote-template?${params}`, {
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
| `id` | string | yes | The quote template id |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "createdBy": {
        "id": "string",
        "name": "Ava Chen",
        "personId": "string"
      },
      "customerReference": "string",
      "id": "string",
      "isBlocked": true,
      "isOutdated": true,
      "isSepaAuthorization": true,
      "json": "string",
      "lastUpdatedApprovalStatus": "string",
      "paymentTerm": {
        "days": "string",
        "id": "string",
        "method": "string",
        "name": "Ava Chen"
      },
      "quoteNumber": "string",
      "quotestatus": {
        "color": "string",
        "id": "string",
        "label": "string"
      },
      "quoteSubject": "string",
      "quotetemplate": {
        "id": "string",
        "name": "Ava Chen"
      },
      "receivers": {
        "bcc": [
          {
            "email": "ava@example.com",
            "name": "Ava Chen"
          }
        ],
        "to": [
          {
            "email": "ava@example.com",
            "name": "Ava Chen"
          }
        ]
      },
      "salesId": "string",
      "sentAt": "string",
      "totalExcl": 1,
      "totalIncl": 1,
      "totalVat": 1,
      "updatedAt": "string",
      "validDays": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string |  |
| `createdBy.id` | string |  |
| `createdBy.name` | string |  |
| `createdBy.personId` | string |  |
| `customerReference` | string |  |
| `id` | string |  |
| `isBlocked` | boolean |  |
| `isOutdated` | boolean |  |
| `isSepaAuthorization` | boolean |  |
| `json` | string |  |
| `lastUpdatedApprovalStatus` | string |  |
| `paymentTerm.days` | string |  |
| `paymentTerm.id` | string |  |
| `paymentTerm.method` | string |  |
| `paymentTerm.name` | string |  |
| `quoteNumber` | string |  |
| `quotestatus.color` | string |  |
| `quotestatus.id` | string |  |
| `quotestatus.label` | string |  |
| `quoteSubject` | string |  |
| `quotetemplate.id` | string |  |
| `quotetemplate.name` | string |  |
| `receivers.bcc[].email` | string |  |
| `receivers.bcc[].name` | string |  |
| `receivers.to[].email` | string |  |
| `receivers.to[].name` | string |  |
| `salesId` | string |  |
| `sentAt` | string |  |
| `totalExcl` | number |  |
| `totalIncl` | number |  |
| `totalVat` | number |  |
| `updatedAt` | string |  |
| `validDays` | number |  |

## Native endpoint

Through the native Simplicate API, this operation is `GET /sales/quote/:id` (base URL `https://{{credentials.subdomain}}/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-quote-template.md) for the provider-specific parameters and requirements.

