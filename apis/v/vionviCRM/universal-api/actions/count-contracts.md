# vionvi CRM: Count Contracts

Retrieves the contract count from vionvi CRM.

```
GET https://connect.mindcloud.co/v1/universal/vionviCRM/latest/actions/count-contracts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a vionvi CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vionviCRM/latest/actions/count-contracts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vionviCRM/latest/actions/count-contracts?${params}`, {
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
      "data": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | number | Total contract count returned by the API. |

## Native endpoint

Through the native vionvi CRM API, this operation is `GET /contract/count` (base URL `https://280-crm-api.vionvi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/count-contracts.md) for the provider-specific parameters and requirements.

