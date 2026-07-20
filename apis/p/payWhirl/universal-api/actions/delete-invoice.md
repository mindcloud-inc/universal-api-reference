# PayWhirl: Delete Invoice

Deletes an existing invoice from PayWhirl.

```
DELETE https://connect.mindcloud.co/v1/universal/payWhirl/latest/actions/delete-invoice
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PayWhirl `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/payWhirl/latest/actions/delete-invoice?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/payWhirl/latest/actions/delete-invoice?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "invoice": {
        "amountDue": 1,
        "customerId": 1,
        "deletedAt": "string",
        "id": 1,
        "status": "string"
      },
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `invoice.amountDue` | number |  |
| `invoice.customerId` | number |  |
| `invoice.deletedAt` | string |  |
| `invoice.id` | number |  |
| `invoice.status` | string |  |
| `status` | string |  |

## Native endpoint

Through the native PayWhirl API, this operation is `POST /delete/invoice` (base URL `https://api.paywhirl.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-invoice.md) for the provider-specific parameters and requirements.

