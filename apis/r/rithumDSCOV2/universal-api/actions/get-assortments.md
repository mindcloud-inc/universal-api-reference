# Rithum DSCO: List Assortments

Lists assortments in Rithum DSCO.

```
GET https://connect.mindcloud.co/v1/universal/rithumDSCOV2/latest/actions/get-assortments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rithum DSCO `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rithumDSCOV2/latest/actions/get-assortments?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rithumDSCOV2/latest/actions/get-assortments?${params}`, {
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
      "assortments": [
        {}
      ],
      "scrollId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assortments` | array<object> | DSCO assortments returned by the API. |
| `scrollId` | string | Scroll ID for additional result pages. |

## Native endpoint

Through the native Rithum DSCO API, this operation is `GET assortment` (base URL `https://api.dsco.io/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-assortments.md) for the provider-specific parameters and requirements.

