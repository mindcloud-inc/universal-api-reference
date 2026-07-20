# RollWorks: List ICP Accounts by Advertisable EID

Retrieves ICP accounts in RollWorks by advertisable EID.

```
GET https://connect.mindcloud.co/v1/universal/rollWorks/latest/actions/list-icp-accounts-by-advertisable-eid
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RollWorks `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rollWorks/latest/actions/list-icp-accounts-by-advertisable-eid?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rollWorks/latest/actions/list-icp-accounts-by-advertisable-eid?${params}`, {
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
      "data": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |

## Native endpoint

Through the native RollWorks API, this operation is `POST /audience/v1/ideal_customer_profile/accounts` (base URL `https://services.adroll.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-icp-accounts-by-advertisable-eid.md) for the provider-specific parameters and requirements.

