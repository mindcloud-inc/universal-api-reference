# Synchroteam: List Invoices and Quotations

Retrieves invoices and quotations from Synchroteam using supported filters.

```
GET https://connect.mindcloud.co/v1/universal/synchroteam/latest/actions/list-invoices-and-quotations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Synchroteam `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/synchroteam/latest/actions/list-invoices-and-quotations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/synchroteam/latest/actions/list-invoices-and-quotations?${params}`, {
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
| `filters` | object | no | Optional. Provide the Synchroteam invoice list filters object (per docs). |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": 1,
      "data": {
        "num": 1,
        "numberLines": 1
      },
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | number |  |
| `data.num` | number |  |
| `data.numberLines` | number |  |
| `message` | string |  |

## Native endpoint

Through the native Synchroteam API, this operation is `POST /Api/v2/Invoices/List` (base URL `https://ws.synchroteam.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-invoices-and-quotations.md) for the provider-specific parameters and requirements.

