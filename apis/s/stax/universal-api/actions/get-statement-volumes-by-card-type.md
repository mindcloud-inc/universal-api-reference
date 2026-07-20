# Stax: Get Statement Volumes by Card Type

Retrieves statement volumes by card type from Stax.

```
GET https://connect.mindcloud.co/v1/universal/stax/latest/actions/get-statement-volumes-by-card-type
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stax `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stax/latest/actions/get-statement-volumes-by-card-type?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stax/latest/actions/get-statement-volumes-by-card-type?${params}`, {
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
| `endDate` | string | no | Report interval end date |
| `startDate` | string | no | Report interval start date |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": 1,
      "cardType": "string",
      "count": 1,
      "date": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | number | Processed volume for the card type row. |
| `cardType` | string | Card type label reported by Stax. |
| `count` | number | Number of transactions for the card type row. |
| `date` | string | Statement date represented by the row. |

## Native endpoint

Through the native Stax API, this operation is `GET /query/statement/v3/volumes/card-type` (base URL `https://apiprod.fattlabs.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-statement-volumes-by-card-type.md) for the provider-specific parameters and requirements.

