# RollWorks: Update ICP by ICP EID and Advertisable EID

Updates an ideal customer profile in RollWorks by ICP and advertisable EID.

```
PUT https://connect.mindcloud.co/v1/universal/rollWorks/latest/actions/update-icp-by-icp-eid-and-advertisable-eid
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RollWorks `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/rollWorks/latest/actions/update-icp-by-icp-eid-and-advertisable-eid" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rollWorks/latest/actions/update-icp-by-icp-eid-and-advertisable-eid', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
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

Through the native RollWorks API, this operation is `POST /audience/v1/ideal_customer_profile/:icp_eid` (base URL `https://services.adroll.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-icp-by-icp-eid-and-advertisable-eid.md) for the provider-specific parameters and requirements.

