# RollWorks: Delete ICP by ICP EID and Advertisable EID

Deletes an ideal customer profile from RollWorks by ICP and advertisable EID.

```
DELETE https://connect.mindcloud.co/v1/universal/rollWorks/latest/actions/delete-icp-by-icp-eid-and-advertisable-eid
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RollWorks `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/rollWorks/latest/actions/delete-icp-by-icp-eid-and-advertisable-eid?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rollWorks/latest/actions/delete-icp-by-icp-eid-and-advertisable-eid?${params}`, {
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

Through the native RollWorks API, this operation is `DELETE /audience/v1/ideal_customer_profile/:icp_eid` (base URL `https://services.adroll.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-icp-by-icp-eid-and-advertisable-eid.md) for the provider-specific parameters and requirements.

